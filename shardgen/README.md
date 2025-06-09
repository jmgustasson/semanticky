ShardGen - Create semantic captures of your chat sessions.

To run this, simply copy and paste 'shardgen-v2.1.md' into a live chat session.

Alternatively, you can append a chatlog to the end and change the EXECUTE statement to specify that the operator should use the appended chatlog as input. Be advised, though, that running the operator in an existing session (make sure it's longer than about a dozen exchanges or so) gives you the richest capture, because a simple conversation log is missing a lot of temporal context that is present in a live session.

Files (what you need to run it):
- README.md (instructions are in this file)
- shardgen-v2.1.md - the ShardGen semantic JSON operator

Development, testing, and sample outputs:
- ShardOps 2.0 - Initial Design Specification (in JSON format for clarity)
- ShardGen 2.0 Development Conversation (interim chatlog) - cutoff before first shard run
  - (shard-live) ShardOps v2.0 Redesign (development phase, interim) - live session shard
  - (shard-log) ShardOps v2.0 Redesign (development phase, interim) - shard generated from chatlog file
- ShardGen 2.0 Development Conversation (final chatlog) - entire chatlog of development session
- (shard-live) ShardOps v2.0 Redesign (development phase, final) - live session shard
- ShardOps v2.0 Redesign (test phase and further refinements, session 1) - testing, refinements leading to v2.1
- (shard-live) ShardGen v2.1 Redesign (test and refinement session, final) - live session shard
- Expanding a Shard (sample prompts for querying the "ShardGen v2.1 Redesign" shard

Notes:
1. Three of the shards were generated with v2.0, and one with v2.1, due to the sequence of development. The core engine is the same between both of these, and the differences don't affect the conclusions drawn. For the curious, you can see the differences by searching for compression stuff (taken out in v2.1); also, the refinement session made some of the JSON directives less "academic". This shows what can happen when you develop code and other things in a long chat session; the deliverable can be skewed by the session content. It's important to use progressive chat sessions for development in order to keep the slate as clean as possible, and it can be easy to forget (as you can see). It's still a habit in progress...

2. Some of you might get a chuckle out of my using "rubbish" in the refinement session. And, as expected, the shard captured it and later gave me a mild scolding about being more specific.
