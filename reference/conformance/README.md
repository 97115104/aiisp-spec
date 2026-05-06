# Reference Conformance

Placeholder for AIISP-2 conformance tests.

The conformance suite should eventually verify:

- all examples validate against the Draft v0.1 schemas;
- `POST /v2/inference` rejects missing or unknown categories;
- routers reject models outside the requested category;
- settlement contracts reject duplicate `event_id` values;
- rejected data and DPO records do not mint HDCT;
- public settlement records omit prompt text, completion text, private client identifiers, and secrets;
- inference settlement events include environmental lines.

