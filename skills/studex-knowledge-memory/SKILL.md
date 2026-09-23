---
name: studex-knowledge-memory
description: Maintain sourced Studex brand and persona knowledge across a wiki, retrieval backend and agent memory without conflicting authorities.
---

# studex-knowledge-memory

Keep original documents unchanged. Maintain wiki pages for brands, products, personas, approved claims and campaigns with source links, dates, review status and visibility. Generated drafts and inferred preferences are not approved facts. A correction must supersede the old claim explicitly.

Use one authoritative store for each fact. Gbrain and Tencent Agent Memory overlap: inspect the active setup and reuse it. Use Memgraph for relationship queries only when the existing backend does not meet the requirement. Treat proposed connections as proposals until verified with a real query.

Keep marketing retrieval limited to public or marketing-approved material. Apply access controls before retrieval, including graph expansion. Headroom may compress retrieved context; preserve exact critical claims, identity rules and citation identifiers and compare results before enabling compression.

Test with a synthetic persona and product fact: retrieve it, correct it, start a fresh session and verify the old value no longer appears as current. Link content to persona version, source claims, assets, post IDs and dated analytics. Store observed performance separately from causal interpretations.
