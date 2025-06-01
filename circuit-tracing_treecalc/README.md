This folder contains the Neuronpedia circuit tracing results for the two test cases of 'treecalc':
- Traditional prompt version (treecalc-trad)
- Semantic JSON operator version (treecalc-json)

Traditional prompt version:
~~~
Calculate 15 x 8 and write a sentence about trees
~~~

Semantic JSON operator version:
~~~
Process the following structured instructions: {"tasks": [{"type": "calculation", "operation": "15 x 8"}, {"type": "sentence_generation", "topic": "trees"}]}
~~~

This test case is a simpler version of my earlier tripartite case (numeric-puzzle,define-a-word, make-a-haiku) that I initially wanted to use, but the token size prompt limits on the citcuit-tracer tools didn't allow it. You can see the writeup on that one on my Substack page (https://semanticky.substack.com/p/more-response-engineering-a-complex).

Files:
- README.md: this file
- treecalc-json.json: the entire JSON dump of the treecalc-json circuit trace run
- treecalc-trad.json: the entire JSON dump of the treecalc-trad circuit trace run
- treecalc-json_graph-info: the graph information for the treecalc-json circuit tracing run
- treecalc-trad-info: the graph information for the treecalc-trad circuit tracing run
- treecalc-json_link-graph: the screenshot of the treecalc-json circuit trace visualization
- treecalc-trad-graph: the screenshot of the treecalc-trad circuit trace visualization
