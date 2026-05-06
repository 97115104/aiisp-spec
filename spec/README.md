# spec/

Normative specification documents in the **AIISP** family.

| File | Status | Description |
| --- | --- | --- |
| [`aiisp-2.md`](./aiisp-2.md) | Draft v0.1, May 2026 | Active HDC v2 specification for contributor-aligned inference routing, settlement, HDCT issuance events, environmental lines, and public settlement batches. |
| [`aiisp-1.md`](./aiisp-1.md) | Draft v0.1, April 2026 | Historical/provider-facing draft for request-cost disclosure by centralized inference providers. |

## Schemas

AIISP-2 Draft v0.1 schemas live in [`schemas/aiisp-2/`](./schemas/aiisp-2/):

- `inference-request.schema.json`
- `inference-response.schema.json`
- `settlement-event.schema.json`
- `settlement-batch.schema.json`
- `environmental-line.schema.json`
- `node-manifest.schema.json`
- `contribution.schema.json`
- `dpo-pair.schema.json`

To propose a change, open a pull request against the relevant file. To propose a brand-new spec in the family, see [`../GOVERNANCE.md`](../GOVERNANCE.md) and the [amendment issue template](https://github.com/97115104/aiisp-spec/issues/new?template=amendment.yml).
