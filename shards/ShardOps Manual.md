# ShardOps: Users Guide and Reference

*Analyze conversation patterns to improve your AI interactions*

*NOTE: ShardOps requires an LLM model with a fairly high reasoning capability (such as Claude Sonnet or Opus) to give you the best results. Other models may not capture as deep of patterns if you run this operator on them. However, you can bring the chatlogs from other models to the Claudes and have it generate the shards.

The ShardOps package is in my GitHub directory (the same place that you got this manual).

*PLEASE NOTE:* Since shards are essentially a capture of your interaction style and therefore represent "a shard of your brain," give some thought toward storing them in a secure place, and be mindful of who you share them with. Treat them like you would your original chatlogs.

---
## What is ShardOps?

ShardOps creates structured summaries (called *shards*) of your conversations that capture how you think, solve problems, and interact in a conversational setting. These shards help you identify patterns in your style with an eye toward helping you improving your efforts over time.

A really nice feature is that this version of ShardOps captures your personal voice (register). That way, when you report on the contents of a shard later, the report "sounds like you."

**Why shards matter:** Most people don't realize their interaction patterns significantly affect AI output quality. ShardOps helps you see these patterns clearly.

---
## Quick Start

### Creating a Shard

At the end of any substantial conversation (a dozen prompt/responses or longer), construct and enter the following prompt:

```
[replace this line with the entire ShardOps package]
EXECUTE ShardGen
```

Claude will analyze your chat session and create a shard containing things like your problem-solving patterns, how ideas developed, and interaction dynamics (and more). However, it won't give you any analysis yet; that comes later.

If you are bringing in a chatlog from another LLM, use the following:

```
[replace this line with the entire ShardOps package]
EXECUTE ShardGen on the following chatlog:
---BEGIN CHATLOG---
[replace this line with the external chatlog]
---END CHATLOG---
```

Then, if you want, save the output shard to your PC.

### Seeing what's in your shard

You can try to read the JSON, but there's a much better way: use ShardExpand!

If you previously ran ShardGen in the current conversation, simply enter the following prompt:

```
EXECUTE ShardExpand on the last shard in this conversation.
```

For a shard you created in another conversation, construct the following prompt and enter it into a fresh Claude conversation:

```
[replace this line with the entire ShardOps package]
EXECUTE ShardExpand
[replace this line with your saved shard]
```

Claude will reconstruct the conversation, preserving the thinking patterns and insight development.

ShardExpand is designed to process just one shard. If you want to get fancy, see the "Multi-Shard" section below.

---
## The Two Core Operators

### ShardGen: Create a Shard
Examines conversations and extracts structured summaries of thinking patterns, problem-solving approaches, and interaction dynamics. Works best on substantial exchanges where ideas developed.

### ShardExpand: Tell Me What's in My Shard
Rebuilds conversations from shards, preserving thinking processes and insight development rather than exact words.

---
## Single Shard Analysis

While ShardExpand gives you a core narrative, you can also ask it follow-questions of your own. Here are some examples for you to try. You only need to enter the lines in quotes.

**"What does this shard reveal about my problem-solving approach?"**

The answer will:
- Show whether you iterate and build on responses or if you tend to waver
- Reveal your breakthrough patterns (those "aha" moments)
- Identify collaborative vs. transactional tendencies (do you team up with the LLM, or just treat it as an answer vending machine)

**"Where did I tend to get stuck, and why?"**

Claude will:
- Highlight circular thinking loops
- Show context gaps that could have limited progress
- Reveal missed opportunities for deeper explorations

**"How could this conversation have been more productive?"**

Learn:
- better framing techniques
- where greater specificity would have helped
- about opportunities for strategic follow-up

---
## Multi-Shard Pattern Recognition

You can batch multiple shards together and analyze them without using ShardOps. Just construct the following prompt and enter it into a fresh conversation:

```
[your first shard goes here]
[your next shard goes here]
...
[your last shard goes here]

[your first question set about the shards goes here]
```

(use 3 or more shards for best results)

Here's some sample question sets:

**"What do I consistently do across conversations, both good and bad?"**

Helps you identify:
- how to improve your starting approaches (too broad? insufficient context?)
- see opportunities to work on follow-up habits (building momentum instead of jumping between topics)
- ways to polish up your collaboration style to use Claude's capabilities better

**"How has my conversation style changed over time?"**

This one is my favorite:
- Track improvements in question quality
- See development in problem-solving approaches
- Identify persistent blind spots

**"What consistently limits my effectiveness?"**

Helps you work on the following:
- Patterns you repeat without realizing
- Consistent gaps in your approach
- Underutilized AI capabilities

---
## Conversation Quality Indicators

### Productive Patterns (The Good)

**Clear Development**
- Multiple phases with progression
- Breakthrough moments and insight building
- Increasing complexity and refinement

**Effective Collaboration** 
- Ideas connecting across exchanges
- Building on Claude's responses
- Insights emerging through interaction

**Good Problem Framing**
- Clear context and constraints provided
- Specific examples and background
- Iterative refinement of challenges

### Warning Signs (The Not-So-Good)

**Shallow Engagement**
- One-shot questions without follow-up
- No conversation development
- Treating Claude like a search engine

**Poor Context**
- Vague problem descriptions
- Missing relevant background
- Expecting mind-reading from AI

**Weak Follow-Through**
- Not building on responses
- Jumping between unrelated topics
- Missing opportunities for deeper exploration

---
## Improvement Strategies

### Provide Better Context

**Before:** "Help me with my restaurant project; see the attached stuff."

**After:** "I'm developing a mobile app for local restaurants. I've got basic UI mockups done, but I'm stuck on real-time order tracking. I've considered WebSockets but worry about battery drain. What approaches should I explore?"

Specific context enables targeted assistance instead of generic advice.

### Use Follow-Up Questions

Instead of accepting first responses, try: "Can you dig deeper into the scalability implications?" or "How would this handle edge cases like network timeouts?"

### Think Collaboratively

Treat Claude as a thinking partner who builds on your ideas, not an information dispenser.

---
## Building Your Shard Collection

### Focus on Substantial Conversations
- Problem-solving sessions where you made progress (no need to save "short shards")
- Learning conversations where you grasped new concepts  
- Frustrating chats to understand what went wrong (don't be embarrassed; we've all been there)
- Creative collaborations where ideas developed (these will surprise you)

### Organize Systematically (I left this in, but y'all know what to do)
Use descriptive naming:
- `breakthrough_database_design_2025-06.json`
- `stuck_css_layout_analysis.json`
- `productive_marketing_brainstorm.json`

### Review Regularly (YMMV here)
Periodic analysis:
1. What conversation styles work best for you?
2. How has your interaction quality changed?
3. What consistent gaps appear across conversations?

---
## Advanced Stuff

### Cross-Domain Comparison
Compare shards across different areas:
- Technical vs. creative conversations
- Learning vs. implementation discussions
- Different problem-solving contexts

### Conversation Design
Use insights from successful shards to design better future conversations:
- How do your productive sessions start?
- What follow-up patterns work best?
- How do you most effectively provide context?

### Track Progress
Monitor conversation pattern evolution over time:
- Better problem framing
- More effective iteration
- Improved collaborative momentum

---
## Common Issues

### "My shard seems too simple"
**Cause:** Conversation was too short or shallow  
**Solution:** ShardGen works best on substantial conversations with real development (10-12 conversational exchanges)

### "ShardExpand doesn't match my original words"
**Expected:** Shards preserve thinking patterns, not your exact words  
**Focus:** Whether the problem-solving process feels accurate

### "I can't identify patterns"
**Try:** Analyze 3-5 shards together with specific questions  
**Focus:** Recurring approaches rather than content differences

### "Conversations still feel frustrating"
**Check:** Are you implementing insights from analysis?  
**Remember:** Changing interaction patterns takes practice (and Claude is always willing to help you do that, too)

---
## The Bottom Line

AI quality mirrors your interaction quality. Improve your conversation patterns and you'll see dramatically better results. ShardOps makes those patterns visible so you can refine them systematically.

Give it a go!
