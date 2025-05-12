
For full transparency. I heavily modified this and made my own version. Claude, dude, you've got a ways to go before you can generate completely satisfying user documentation! Of course, my generating prompt might have been too simple (see below). This ask came after the validation and testing of the DuoMap operator. Not saying that mine's perfect, either! Maybe I should run DuoMap against my own version. 🤔

Here's the generating prompt for the Users Guide:

~~~
Julie:

Can you generate me a Users Guide for DuoMap?
~~~

Very simple. And here's what Claude came up with.

# DuoMap User Guide

## Introduction

DuoMap is a semantic JSON operator that generates dual-representation explanations of complex domains. It automatically extracts core concepts from any knowledge domain and creates parallel explanations: one technically precise, the other accessible to a 7-year-old, while maintaining structural isomorphism between the two representations.

## Quick Start

1. Copy the complete DuoMap JSON specification
2. Paste it into a conversation with Claude
3. Add the execution command:
   ```
   EXECUTE DuoMap with domain="[YOUR DOMAIN]" depth="[DEPTH]"
   ```
4. Receive a complete set of concept patterns and application stories

## Parameters

### Domain (Required)
Specify what you want explained. This can be:
- A simple text description (`"Quantum Computing"`)
- A reference to an attachment (`"See attached document"`)
- A URL (`"https://example.com/article"`)
- A specific subdomain (`"Machine Learning: Neural Networks"`)

### Depth (Optional)
Control the complexity and scope of the explanation:
- `fundamental` - Core concepts only with minimal technical details
- `practical` - Application-oriented with moderate technical density (default)
- `comprehensive` - Complete coverage including historical context, edge cases, and comparative approaches

## Output Structure

DuoMap generates two complementary sections:

### 1. Pattern Constellations
Organized groups of dual-representation concept pairs showing how ideas relate to each other:

```
## [Concept Group Name]

**[Pattern Description]:**
{[Simple concept] / [Technical equivalent]}
↓
{[Simple concept] / [Technical equivalent]}
```

The relationships between patterns are indicated by symbols:
- ↓ enables what follows
- ↔ interacts reciprocally
- ↑ builds upon what precedes
- → transforms into
- ← derives from
- ⊂ is contained within
- ⊃ contains

### 2. Application Stories
A set of procedural narratives showing how the concepts work together in practice:

```
## [Procedural Sequence Title]
[Child-accessible narrative with (technical terms) in parentheses]
```

Stories follow the domain's natural procedural organization and include all concepts from the patterns section.

## Best Practices

1. **One Execution Per Session**: For optimal performance, limit DuoMap to one execution per conversation session to prevent complexity drift.

2. **Domain Specificity**: More specific domain requests yield more focused explanations. Compare:
   - Too broad: `"Physics"`
   - Better: `"Classical Mechanics"`
   - Ideal: `"Newton's Laws of Motion"`

3. **Depth Selection**: Choose depth based on your needs:
   - `fundamental` for quick conceptual understanding
   - `practical` for applied knowledge (default)
   - `comprehensive` for in-depth expertise

4. **Content Sources**: DuoMap works with:
   - General knowledge domains
   - Specific documents (upload before executing)
   - Web content (provide URL)
   - Technical specifications

5. **Pattern Analysis**: Look for relationship symbols between patterns to understand conceptual dependencies and interactions.

## Examples

### Example 1: Technical Protocol
```
EXECUTE DuoMap with domain="HTTPS Protocol" depth="practical"
```

### Example 2: Scientific Concept
```
EXECUTE DuoMap with domain="Photosynthesis" depth="fundamental"
```

### Example 3: Attached Document
```
EXECUTE DuoMap with domain="See attached research paper" depth="comprehensive"
```

### Example 4: Abstract Concept
```
EXECUTE DuoMap with domain="Game Theory" depth="practical"
```

## How It Works

DuoMap follows a carefully designed process:

1. **Concept Extraction**: Identifies the minimal spanning set of technical concepts needed to understand the domain.

2. **Pattern Organization**: Establishes relationships between concepts and organizes them into related groups.

3. **Thematic Domain Selection**: Chooses an appropriate child-accessible thematic world (like playground, kitchen, etc.) based on structural fit with the technical domain.

4. **Isomorphism Creation**: Creates precise mappings between technical concepts and their child-accessible equivalents within the selected thematic domain.

5. **Story Generation**: Produces application narratives based on the domain's natural procedural structure, showing how concepts work together.

Throughout this process, DuoMap maintains strict isomorphism between technical and simple representations while ensuring all simple explanations remain within the same thematic domain for consistency.

## Limitations

- DuoMap performs best with one execution per conversation session
- Very broad domains may yield more general explanations
- Extremely specialized technical domains may have fewer intuitive child-mode analogues
- The operator prioritizes structural isomorphism over specialized terminology

## Conclusion

DuoMap bridges the gap between technical precision and intuitive understanding by creating dual-mode explanations of any knowledge domain. By maintaining structural isomorphism between technical concepts and child-accessible analogues, it makes complex subjects approachable without sacrificing accuracy.

Use DuoMap to:
- Learn new technical domains
- Create educational materials
- Simplify complex concepts
- Identify core principles in any field
- Develop intuitive understanding of abstract ideas