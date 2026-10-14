# Students — TYPESENSE

**Project:** TYPESENSE  
**Category:** SEARCH_ENGINES  
**Upstream:** https://github.com/typesense/typesense.git  
**Pinned commit:** `4f8f4a29e82921a6bae609eb1c07bbda97541cf1`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `5c518443bbd6707f9cb2ce47893eae42317c4cdbfedc11902e32ec41d1795624`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `4f8f4a29e82921a6bae609eb1c07bbda97541cf1`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `5c518443bbd6707f9cb2ce47893eae42317c4cdbfedc11902e32ec41d1795624`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
