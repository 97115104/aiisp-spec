# AIISP Reference Implementation

This directory is reserved for MIT-licensed reference code for the AIISP standards family.

AIISP-2 reference work is split into four parts:

- `contracts/` - HDCT token and settlement contract reference design.
- `router/` - HTTP router, category selection, node dispatch, and batch writer.
- `node/` - Minimal inference-node adapter and manifest behavior.
- `conformance/` - Schema, routing, duplicate-event, and settlement tests.

The reference implementation is not normative unless a future specification explicitly says so. The normative AIISP-2 text lives in [`../spec/aiisp-2.md`](../spec/aiisp-2.md), and the normative Draft v0.1 schemas live in [`../spec/schemas/aiisp-2/`](../spec/schemas/aiisp-2/).

