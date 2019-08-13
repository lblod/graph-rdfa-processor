# graph-rdfa-processor

Note: this module is auto published to npm on CircleCI. Only run `npm version
patch|minor|major` and let CI do the rest.

Green turtle GraphRdfaProcessor extracted and available as a
standalone commonJS / ES2015 module.

All credits are due to Alex Milowski for
[green-turtle](https://github.com/alexmilowski/green-turtle).

Aside from the adaptation to ES2015, some little changes were made to
make it compatible with [jsdom](https://github.com/tmpvar/jsdom). Also
proper Errors are now thrown instead of plain strings.

For convenience, a high level API has been added:

```js
import getRdfaGraph from graph-rdfa-processor;

let opts = {baseURI: 'http://example.com'};
let graph = getRdfaGraph(documentOrNode, opts);
console.log(graph.toString());
```

See the tests for a full example.

## RDFa to JSON-LD

see
[jsonld-rdfa-parser](https://github.com/science-periodicals/jsonld-rdfa-parser)
(using this module to extract the RDFa graph.
