# Reference Contracts

Placeholder for AIISP-2 settlement contracts.

The reference contract package should eventually include:

- an ERC-20 HDCT implementation for local test chains and Base-compatible deployments;
- a settlement contract that records event identifiers and rejects duplicate mints;
- batch settlement helpers;
- events exposing `event_id`, `event_type`, `category`, `contributor`, `hdct_amount`, and `batch_id`;
- tests for duplicate event rejection and rejected contribution behavior.

AIISP-2 requires event-based issuance only. Contract code in this directory must not implement recurring royalties for prior data use.

