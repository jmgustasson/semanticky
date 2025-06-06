ShardOps - a system to capture and report on interesting patterns in your chat conversations.

ShardOps uses a sophisticated mathematical model to capture and analyze patterns from your chat sessions.
The capture is in JSON format, and is called a *shard*.
You can learn a lot about your conversation style from shards. Also, you can batch up 3 or more shards to see
persistent habits across sessions. I've benefitted greatly from this capability.
A really cool feature is that the shard report is aligned with your conversational "style" (register),
so that reading it "feels" like you are reading the original chatlog (despite the difference in words).
In other words, the shard captures how you sound!

REQUIREMENTS:
This operator package requires a model such as Claude Sonnet/Opus.
However, you can analyze chatlogs from other LLMs. See the instructions for details.

FILES:
- README.md - this file
- shardops-v1.2.md
  - a package containing the two operators (ShardGen and ShardExpand)
- ShardOps Manual.md - full instructions on how to use the system

Full disclosures on development process:
- I came up with the original requirements for the system and the information theory aspects underlying it
- Claude and I iterated to find the best math framework to use for the final design
- Claude crafted the final JSON operators (this is a symmetry requirement for semantic JSON operators)
- We validated and tested the entire thing
- Claude created the manual draft outline and I heavily edited it

For more information about semantic JSON operators, see my Substack at:
   https://substack.com/@semanticky

This system is free for anyone to use and modify.

*PLEASE NOTE:* Since shards are essentially a capture of your interaction style and therefore represent "a shard of your brain," give some thought toward storing them in a secure place, and be mindful of who you share them with. Treat them like you would your original chatlogs.
