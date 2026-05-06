# Reference Router

Placeholder for the AIISP-2 router reference implementation.

The router should eventually:

- expose `POST /v2/inference`;
- require `X-AIISP-Category`;
- select registered Category Models and eligible Inference Nodes;
- preserve OpenAI-compatible request and response bodies where practical;
- create settlement events and settlement batches;
- attach environmental lines to inference events;
- avoid writing prompts, completions, private client identifiers, or secrets to public settlement records.

