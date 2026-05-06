# Reference Node

Placeholder for an AIISP-2 inference-node adapter.

The node adapter should eventually:

- publish a manifest matching `spec/schemas/aiisp-2/node-manifest.schema.json`;
- serve one or more registered Category Models;
- sign serving evidence for completed inference work;
- expose health and version endpoints;
- report measured or estimated environmental data according to the node manifest.

