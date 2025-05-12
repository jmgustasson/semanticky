

# DuoMap User's Guide (Julie's Version)
(note: the initial version of this document was created by Claude; I've heavily edited it because I wasn't happy with the flow. For transparency, I've included Claude's version in the same GitHub repository directory as this file)

## Introduction

DuoMap is a semantic JSON operator that lowers the accessibility bar for unfamiliar topics. It creates pattern pairs in {simple, technical} form, then creates a "constellation" that shows dependency relationships between the patterns, and finally, creates a child-accessible story about them (with the technical points in parentheses). If you're a subject matter expert in the topic, this will seem extremely trivial. But if not, you (and maybe your kids) will find it extremely useful. Even if you are an expert, this will provide a very useful "survey" of the material. Try running a PDF from arxiv through it and see. And then try it out on your own created works, too. It can give you a reading of how coherent it is.

Enjoy!

## Quick Start
1. Copy the complete DuoMap JSON specification (available in the same GitHub subfolder as this guide) somewhere handy.
2. At the bottom (the VERY bottom, outside the JSON spec), you will see an EXECUTE directive:
   ```
   EXECUTE DuoMap with domain="[YOUR DOMAIN]" depth="[DEPTH]"
   ```
3. Fill in the domain and depth (see the Parameters section below).
4. Paste the modified version in its entirety into a new LLM conversation.

## Parameters

### Domain (Required)
What you want explained. This can be:
- A simple text description (`"Quantum Computing"`)
- A reference to an attachment (`"See attached document"`)
- A URL to a web page
- A specific subtopic (`"Machine Learning: Neural Networks"`)
See the "Best Practices" and "Examples" section below.

### Depth (Optional)
Control the complexity and scope of the explanation:
- `fundamental` - Core concepts only with minimal technical details
- `practical` - Application-oriented with moderate technical density (default)
- `comprehensive` - Complete coverage including historical context, edge cases, and comparative approaches

## Output
DuoMap generates two complementary sections:

### 1. Pattern Constellations
Organized groups of dual-representation concept pairs showing how ideas relate to each other:

```
## [Concept Group Name]

**[Pattern Description]:**
{[Simple concept] / [Technical equivalent]}
↓
{[Simple concept] / [Technical equivalent]}
→

... more patterns and relationship symbols ...

```

The relationships between patterns are indicated by symbols:
- ↓ enables what follows
- ↔ interacts reciprocally
- ↑ builds upon what precedes
- → transforms into
- ← derives from
- ⊂ is contained within
- ⊃ contains
(note: Don't assume associativity here! I've thought about adding parentheses to the patterns to show nesting dependencies...)

### 2. Application Stories
A set of procedural narratives showing how the concepts work together in practice:
```
## [Procedural Sequence Title]
[Child-accessible narrative with (technical terms) in parentheses]
```
Stories follow the domain's natural procedural organization and include all concepts from the patterns section.

## Best Practices
1. **One Execution Per Session**: For optimal performance, limit DuoMap to one execution per conversation session to prevent "complexity drift". If you're clever, you can issue prompts to "reset" the session. This becomes more important with LLMs that remember your conversational history.
2. **Domain Specificity**: More specific domain requests yield more focused explanations. Compare:
   - Too broad: `"Physics"`
   - Better: `"Classical Mechanics"`
   - Ideal: `"Newton's Laws of Motion"`
3. **Outputs:** As always, independently VERIFY them against other sources.

## Examples
You can see the outputs from the first two examples in the GitHub subfolder, along with some interesting observations. 

### Example 1: Technical Protocol
```
EXECUTE DuoMap with domain="HTTPS Protocol" depth="practical"
```

### Example 2: Scientific Concept
```
EXECUTE DuoMap with domain="Photosynthesis in roses" depth="fundamental"
```

### Example 3: Using an Attached Document
```
EXECUTE DuoMap with domain="See attached document below" depth="comprehensive"
```

### Example 4: URL (assuming it's not robot-protected!)
```
EXECUTE DuoMap with domain="https://somewhere.com/article/..." depth="practical"
```

## How It Works (Advanced)

DuoMap follows a carefully designed process:

1. **Concept Extraction**: Identifies the minimal spanning set of technical concepts needed to understand the domain. The LLM determines the overall map on its own.
2. **Pattern Organization**: Establishes relationships between concepts and organizes them into related groups to form a fundamental "constellation." Those of you with extensive graph theory knowledge can probably come up with a better name. "Constellation" works for me.
3. **Thematic Domain Selection**: Chooses an appropriate child-accessible thematic world (like playground, kitchen, LEGOs, etc.) based on structural fit with the technical domain. I thought about allowing a "THEMATIC" parameter, but ultimately decided this would restrict the best possible "child mode" explanation. Sometimes the entire world cannot be explained by LEGO analogies!
4. **Isomorphism Creation**: Creates precise mappings between technical concepts and their child-accessible equivalents within the selected thematic domain.
5. **Story Generation**: Produces application narratives based on the domain's natural procedural structure, showing how concepts work together.

