# Ethics — TYPESENSE

**Project:** TYPESENSE  
**Category:** SEARCH_ENGINES  
**Upstream:** https://github.com/typesense/typesense.git  
**Pinned commit:** `4f8f4a29e82921a6bae609eb1c07bbda97541cf1`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `5c518443bbd6707f9cb2ce47893eae42317c4cdbfedc11902e32ec41d1795624`  
**Date:** October 2026

## Position

TYPESENSE is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
