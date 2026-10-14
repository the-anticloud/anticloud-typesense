# Educators — TYPESENSE

**Project:** TYPESENSE  
**Category:** SEARCH_ENGINES  
**Upstream:** https://github.com/typesense/typesense.git  
**Pinned commit:** `4f8f4a29e82921a6bae609eb1c07bbda97541cf1`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `5c518443bbd6707f9cb2ce47893eae42317c4cdbfedc11902e32ec41d1795624`  
**Date:** October 2026

## Teaching with TYPESENSE

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `5c518443bbd6707f9cb2ce47893eae42317c4cdbfedc11902e32ec41d1795624` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
