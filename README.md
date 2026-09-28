# Parivartan — Site Change Ledger

Offline, open-weight AI that turns construction instructions into a traceable BOQ change ledger.

**Status:** Planning and early development for Frogtoberfest 2026 Nepal. This repository currently documents the proposed product; a working application and measured results are not available yet.

## Problem

Small construction and hydropower teams receive revised instructions across PDFs, correspondence and spreadsheets. Engineers must manually determine which BOQ items are affected and which earlier instructions have been replaced. Missed revisions, duplicate changes and incomplete information can lead to inaccurate quantity estimates, rework, delays and disputes.

## Proposed solution

Parivartan will connect each instruction to the relevant BOQ item and maintain a reviewable history of active, duplicate, superseded and unresolved changes. Engineers will see source evidence, quantity calculations and missing information before accepting a change.

## How AI powers the product

A locally hosted open-weight Qwen model will extract structured fields from instruction text, match work descriptions to BOQ items and propose amendment relationships. Validated JSON output will drive change-record creation, exception routing and inputs to deterministic calculations. Engineers will review the evidence before changes enter the accepted ledger. AI will not invent rates, approve designs or determine contractual entitlement.

Planned pipeline: BOQ + instruction documents → local AI extraction and matching → schema/evidence checks → proposed events and clarification queries → engineer review → deterministic ledger and exports.

## October MVP scope

- English typed instructions and text-based PDFs
- BOQ CSV import, with XLSX considered after the core works
- Quantity changes, explicit replacement instructions and unresolved conflicts
- Duplicate detection and version history
- Evidence-linked review, unit checks and limited quantity formulas
- CSV export and a print-friendly change register

Full CAD interpretation, structural design, autonomous approvals and automatic correspondence are outside the MVP.

## Planned stack

React + TypeScript + Vite, Python + FastAPI + Pydantic, SQLite, pdfplumber and Ollama. Initial model candidate: Qwen3-4B Q4_K_M, subject to local accuracy and latency testing. No proprietary AI API is planned in the product pipeline.

## Evaluation and sample data

We plan to publish original synthetic construction examples and test BOQ matching, source support, unit-safe arithmetic, duplicate handling and supersession. Evaluation results and installation instructions will be added when implemented. No confidential employer documents will be included.

## Team

A two-person Nepal-based team combining civil/hydropower engineering experience with CSIT programming skills. Domain work covers sample data, engineering validation and user testing; software work covers application development, integration and testing.

## Roadmap

1. Working local extraction and reconciliation core
2. Evidence review interface and export
3. Edge-case tests, user feedback and evaluation
4. Reproducible setup, documentation and demonstration

## License

Original repository content is released under the MIT License. Third-party models and dependencies retain their own licenses; model weights are not included. Any future dataset will have its own explicit license.
