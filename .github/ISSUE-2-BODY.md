# AIISP-2 v0.1 — Public review and comment thread

> **Specification:** [`aiisp-2.md`](https://github.com/97115104/aiisp-spec/blob/main/spec/aiisp-2.md) · **Companion paper:** [`human-data-collective-v2.md`](https://github.com/97115104/aiisp-spec/blob/main/paper/v2/human-data-collective-v2.md) · **Status:** Draft (v0.1, May 2026) · **Editor:** Austin Harshberger ([`x@97115104.com`](mailto:x@97115104.com)) · **License:** CC BY 4.0 (text), MIT (reference code)

This issue is the **primary public-comment thread** for AIISP-2, the second specification in the Human Data Collective standards family. It defines a contributor-aligned inference routing and settlement protocol for a network of category-specific models, distributed inference nodes, and event-based HDCT issuance.

AIISP-2 supersedes AIISP-1 as the active HDC draft. AIISP-1 remains a historical provider-facing disclosure draft. See the [AIISP-1 issue](https://github.com/97115104/aiisp-spec/issues/1) for its comment thread and the version shift diagram in the companion paper for a summary of what changed.

---

## How to comment

Please use the channel that fits your comment. All channels are read.

| If you want to… | Use this |
| --- | --- |
| Add a general comment, question, or reaction | Reply on this thread |
| File a structured objection against a numbered section | [New **Comment** issue](https://github.com/97115104/aiisp-spec/issues/new?template=comment.yml) |
| Propose a substantive amendment, new header, or new behaviour | [New **Amendment** issue](https://github.com/97115104/aiisp-spec/issues/new?template=amendment.yml) |
| Report a typo, broken link, or arithmetic error | [New **Errata** issue](https://github.com/97115104/aiisp-spec/issues/new?template=errata.yml) |
| Suggest specific text in the spec | Open a [Pull Request](https://github.com/97115104/aiisp-spec/pulls) against `aiisp-2.md` |
| Comment on the companion paper (no GitHub account needed) | Select text at **[humandatacollective.org](https://humandatacollective.org)** and attach an inline comment |
| Suggest prose or citation changes to the companion paper | Open a [Pull Request](https://github.com/97115104/aiisp-spec/pulls) against `paper/v2/human-data-collective-v2.md` |
| Comment privately (conflict of interest, security) | Email the editor at [`x@97115104.com`](mailto:x@97115104.com) |

If you are commenting in a professional capacity or on behalf of an organization that would be affected by this standard (inference operator, frontier provider, regulator, civil-society group, worker organization), please **disclose that affiliation in your comment**. The structured templates ask for this explicitly. See [`CONTRIBUTING.md`](https://github.com/97115104/aiisp-spec/blob/main/CONTRIBUTING.md) and [`GOVERNANCE.md`](https://github.com/97115104/aiisp-spec/blob/main/GOVERNANCE.md) for the full process.

---

## What AIISP-2 specifies, in one paragraph

A Client sends an inference request to an AIISP-2 Router carrying a model category and optional node preference. The Router selects an Inference Node and Category Model, forwards the request, receives a metered response, and returns it to the client while creating a Settlement Batch record. The Settlement Contract on Base records the batch, mints Human Data Collective Tokens (HDCT) for each qualifying verified work event — accepted data contribution, verified inference served, accepted DPO feedback pair — and routes an environmental line to carbon and water remediation funds. HDCT issuance is event-based and non-recurring: a recorded event cannot be reminted. Clients and nodes that do not implement the full standard can participate in a degraded mode; the wire format is designed to layer over any existing HTTP inference API.

Full normative text is in [`aiisp-2.md`](https://github.com/97115104/aiisp-spec/blob/main/spec/aiisp-2.md). The companion paper, *The Human Data Collective v2*, provides the full motivation and design rationale at [`paper/v2/human-data-collective-v2.md`](https://github.com/97115104/aiisp-spec/blob/main/paper/v2/human-data-collective-v2.md).

---

## Open questions where reviewer input is most needed

The draft has known gaps. Comments on any of the points below are explicitly invited; please file them as structured **Comment** or **Amendment** issues so they can be tracked and resolved into the next revision.

### 1. HDCT legal classification and securities treatment

HDCT is modeled as an ownership-adjacent speculative token with economic exposure to future network value — the companion paper uses a stock-share analogy explicitly. **What is the correct regulatory classification in key jurisdictions, and what must be true of the governance and distribution design before a public listing or secondary market transfer can proceed?** Comments on Howey analysis, MiCA treatment, and non-US frameworks are invited.

### 2. Contribution verification and fraud resistance

Accepted-work events trigger HDCT minting. The spec leaves contribution review policy, verifier selection, and rejection appeals to later governance documents. **What adversarial surface does event-based issuance create — identity fraud, prompt laundering through intermediate models, collusion to inflate measured contribution — and what verification primitives should be normative in the spec versus advisory?**

### 3. Model collapse and synthetic data gating

The companion paper notes that if contributors flood the data registry with model-assisted output, the Collective's category models could degrade in the same way frontier training pipelines do. **Should AIISP-2 normatively require a model-assisted-work disclosure field in the contribution schema, and what automated or human gate should reject contributions that fail it?**

### 4. Environmental line legitimacy

The spec routes a `C_env` line to carbon and water remediation funds on each settled inference request. **What on-chain or off-chain evidence is required to demonstrate that a credited carbon retirement or water restoration certificate corresponds to real remediation in an affected community, and who audits it?** The Atacama and Cerrillos cases in the companion paper are the motivating cases.

### 5. PoAIC staking and governance rights

The companion paper raises Proof of AI Contribution as a future mechanism for locking earned HDCT as a quality bond, with possible governance rights or additional yield. V2 defers this design. **Should PoAIC be specified as a voluntary worker tier, a node quality bond, a non-transferable reputation score, or left entirely to a later draft?** Early design input is useful before HDCT issuance begins.

### 6. Bootstrapping credibility and milestones

Phased adoption in Section 6 of the companion paper names credible milestones: a working AIISP-2 implementation, at least 1,000 verified contributors or beta sign-ups, a first category-specific model when data permits, and a measurable inference workload served by contributor nodes. **Are these milestones the right ones, and are there external commitments — compute pre-commitments, institutional data partnerships, public interest grants — that reviewers can point to or are willing to make?**

### 7. Non-crypto settlement track

Settlement on Base in HDCT presupposes that a contributor has access to a Base-compatible wallet, on-ramp infrastructure, and a workable jurisdiction. **For contributors and communities for whom that is not true, should AIISP-2 specify a fiat-bridge or direct-grant settlement track as a binding mode, and what is the minimum viable design?**

### 8. Reference implementation and conformance

The spec commits to a reference implementation and conformance suite, both pending. **Which arithmetic checks, schema checks, routing checks, and on-chain settlement checks should be conformance-required versus advisory?** Comments now inform the test suite design before implementation begins.

---

## Comment window

This thread is open indefinitely. Substantive comments received **on or before 2026-07-31** will be reflected in AIISP-2 v0.2, which will be circulated as a separate issue with a diff against v0.1. Earlier amendments may land in interim editorial drafts; see [`CHANGELOG.md`](https://github.com/97115104/aiisp-spec/blob/main/CHANGELOG.md).

---

## Disclosure

The editor (Austin Harshberger) is the principal of Happy Stack Calculus LLC, which intends to operate the reference implementation of AIISP-2 and to act as the initial on-chain settlement infrastructure operator and genesis HDCT minter. This is a present and ongoing conflict of interest. The medium-term plan, documented in [`GOVERNANCE.md`](https://github.com/97115104/aiisp-spec/blob/main/GOVERNANCE.md), is to migrate ratification authority for AIISP-2 v1.0 and beyond to a multi-stakeholder body before the standard is declared stable. The editor's compensation, once any settlement flows exist, will be published on the same on-chain ledger as contributor compensation.

---

## How to cite this draft

```bibtex
@misc{aiisp2spec2026,
  author       = {Harshberger, Austin},
  title        = {AIISP-2: Contributor-Aligned Inference Routing and Settlement Protocol},
  year         = {2026},
  month        = may,
  howpublished = {\url{https://github.com/97115104/aiisp-spec}},
  note         = {Draft v0.1; public review at \url{https://github.com/97115104/aiisp-spec/issues/2}}
}
```

GitHub also surfaces a "Cite this repository" button via [`CITATION.cff`](https://github.com/97115104/aiisp-spec/blob/main/CITATION.cff).

---

Thank you for reading. Pushback is the point.

— A H
