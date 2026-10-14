# TYPESENSE

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-search_engines-lightgrey)

> Anticloud-hardened packaging of the upstream project `TYPESENSE` in category **SEARCH ENGINES**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SEARCH ENGINES · **Upstream:** https://github.com/typesense/typesense.git · **Upstream pin:** `82c53eae44fca30bcf7a86d0b239b1e3e79b212d` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

<p align="center">
  <a href="https://typesense.org">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="assets/typesense_logo_dark.svg">
      <img src="assets/typesense_logo.svg" alt="Typesense" width="600" />
    </picture>
  </a> 
</p>
<p align="center">
  Typesense is a fast, typo-tolerant search engine for building delightful search experiences.
</p>

<p align="center">
  An Open Source Algolia Alternative & <br>
  An Easier-to-Use ElasticSearch Alternative
</p>

<p align="center">
 <!-- <a href="https://circleci.com/gh/typesense/typesense"><img src="https://circleci.com/gh/typesense/typesense.svg?style=shield&circle-token=82c53eae44fca30bcf7a86d0b239b1e3e79b212d"></a> -->
 <a href="https://hub.docker.com/r/typesense/typesense/tags"><img src="https://img.shields.io/docker/pulls/typesense/typesense"></a>
  <a href="https://github.com/typesense"><img src="https://img.shields.io/github/stars/typesense/typesense?label=github%20stars&style=flat"></a><br>
  <a href="https://cloud.typesense.org"><img src="https://img.shields.io/badge/searches_per_month_on_typesense_cloud-10 Billion-blue"></a>
<p>
<p align="center">
  <a href="https://typesense.org">Website</a> | 
  <a href="https://typesense.org/docs/">Documentation</a> | 
  <a href="https://typesense.link/roadmap">Roadmap</a> | 
  <a href="https://typesense.link/slack-community">Slack Community</a> | 
  <a href="https://threads.typesense.org/">Community Threads</a> | 
  <a href="https://twitter.com/typesense">Twitter</a>
</p>
<br>
<p align="center">
  <img src="assets/typesense_books_demo.gif?raw=true" alt="Typesense Demo" width="459" />
</p>

✨ Here are a couple of **live demos** that show Typesense in action on large datasets:

- Search a 32M songs dataset from MusicBrainz: [songs-search.typesense.org](https://songs-search.typesense.org/)
- Search a 28M books dataset from OpenLibrary: [books-search.typesense.org](https://books-search.typesense.org/)
- Search a 2M recipe dataset from RecipeNLG: [recipe-search.typesense.org](https://recipe-search.typesense.org/)
- Search 1M Git commit messages from the Linux Kernel: [linux-commits-search.typesense.org](https://linux-commits-search.typesense.org/)
- Spellchecker with type-ahead, with 333K English words: [spellcheck.typesense.org](https://spellcheck.typesense.org/)
- An E-Commerce Store Browsing experience: [ecommerce-store.typesense.org](https://ecommerce-store.typesense.org/)
- GeoSearch / Browsing experience: [airbnb-geosearch.typesense.org](https://airbnb-geosearch.typesense.org/)
- Search / Browse xkcd comics by topic: [xkcd-search.typesense.org](https://xkcd-search.typesense.org/)
- Semantic / Hybrid search on 300K HN comments: [hn-comments-search.typesense.org](https://hn-comments-search.typesense.org)

🗣️ 🎥 If you prefer watching videos:

- Here's one where we introduce Typesense and show a walk-through: https://youtu.be/F4mB0x_B1AE?t=144
- Check out Typesense's recent mention during Google I/O Developer Keynote: https://youtu.be/qBkyU1TJKDg?t=2399
- Here's one where one of our community members gives an overview of Typesense and shows you an end-to-end demo: https://www.youtube.com/watch?v=kwtHOkf7Jdg

## Quick Links

- [Features](#features)
- [Benchmarks](#benchmarks)
- [Roadmap](#roadmap)
- [Who's using this](#whos-using-this)
- [Install](#install)
- [Quick Start](#quick-start)
- [Step-by-step Walk-through](#step-by-step-walk-through)
- [API Documentation](#api-documentation)
- [API Clients](#api-clients)
- [Search UI Components](#search-ui-components)
- [FAQ](#faq)
- [Support](#support)
- [Contributing](#contributing)
- [Getting Latest Updates](#getting-latest-updates)
- [Build from Source](#build-from-source)

## Features

- **Typo Tolerance:** Handles typographical errors elegantly, out-of-the-box.
- **Simple and Delightful:** Simple to set-up, integrate with, operate and scale.
- **⚡ Blazing Fast:** Built in C++. Meticulously architected from the ground-up for low-latency (<50ms) instant searches.
- **Tunable Ranking:** Easy to tailor your search results to perfection.
- **Sorting:** Dynamically sort results based on a particular field at query time (helpful for features like "Sort by Price (asc)").
- **Faceting & Filtering:** Drill down and refine results.
- **Grouping & Distinct:** Group similar results together to show more variety.
- **Federated Search:** Search across multiple collections (indices) in a single HTTP request.
- **Geo Search:** Search and sort by results around a latitude/longitude or within a bounding box.
- **Vector Search:** Index embeddings from your machine learning models in Typesense and do a nearest-neighbor search. Can be used to build similarity search, semantic search, visual search, recommendations, etc.
- **Semantic / Hybrid Search:** Automatically generate embeddings from within Typesense using built-in models like S-BERT, E-5, etc or use OpenAI, PaLM API, etc, for both queries and indexed data. This allows you to send JSON data into Typesense and build an out-of-the-box semantic search + keyword search experience.
- **Conversational Search (Built-in RAG):** Send questions to Typesense and have the response be a fully-formed sentence, based on the data you've indexed in Typesense. Think ChatGPT, but over your own data.
- **Natural Language Search:** LLM-powered intent detection & query understanding, that converts any free-form natural language phrases into structured filters, sorts and queries.
- **Image Search:** Search through images using text descriptions of their contents, or perform similarity searches, using the CLIP model.
- **Voice Search:** Capture and send query via voice recordings - Typesense will transcribe (via Whisper model) and provide search results.
- **Scoped API Keys:** Generate API keys that only allow access to certain records, for multi-tenant applications.
- **JOINs:** Connect one or more collections via common reference fields and join them during query time. This allows you to model SQL-like r

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **C/C++ / CMake** (manifests: CMakeLists.txt; scanned in UPSTREAM_CLONE)
- Top-level source layout: `api_tests/`, `assets/`, `bazel/`, `benchmark/`, `cmake/`, `debian-pkg/`, `docker/`, `include/`, `src/`, `test/`, `tests/`
- Snapshot size: **298 files**, **151843 lines of code** (measured; see Benchmarks)
- Primary languages: `.h` (103), `.cpp` (77), `.build` (24), `(none)` (20), `.patch` (13), `.dockerfile` (10)
- Upstream commit pinned for this packaging: `82c53eae44fca30bcf7a86d0b239b1e3e79b212d`

---

## Installation

</p>

<p align="center">
  An Open Source Algolia Alternative & <br>
  An Easier-to-Use ElasticSearch Alternative
</p>

<p align="center">
 <!-- <a href="https://circleci.com/gh/typesense/typesense"><img src="https://circleci.com/gh/typesense/typesense.svg?style=shield&circle-token=82c53eae44fca30bcf7a86d0b239b1e3e79b212d"></a> -->
 <a href="https://hub.docker.com/r/typesense/typesense/tags"><img src="https://img.shields.io/docker/pulls/typesense/typesense"></a>
  <a href="https://github.com/typesense"><img src="https://img.shields.io/github/stars/typesense/typesense?label=github%20stars&style=flat"></a><br>
  <a href="https://cloud.typesense.org"><img src="https://img.shields.io/badge/searches_per_month_on_typesense_cloud-10 Billion-blue"></a>
<p>
<p align="center">
  <a href="https://typesense.org">Website</a> | 
  <a href="https://typesense.org/docs/">Documentation</a> | 
  <a href="https://typesense.link/roadmap">Roadmap</a> | 
  <a href="https://typesense.link/slack-community">Slack Community</a> | 
  <a href="https://threads.typesense.org/">Community Threads</a> | 
  <a href="https://twitter.com/typesense">Twitter</a>
</p>
<br>
<p align="center">
  <img src="assets/typesense_books_demo.gif?raw=true" alt="Typesense Demo" width="459" />
</p>

✨ Here are a couple of **live demos** that show Typesense in action on large datasets:

- Search a 32M songs dataset from MusicBrainz: [songs-search.typesense.org](https://songs-search.typesense.org/)
- Search a 28M books dataset from OpenLibrary: [books-search.typesense.org](https://books-search.typesense.org/)
- Search a 2M recipe dataset from RecipeNLG: [recipe-search.typesense.org](https://recipe-search.typesense.org/)
- Search 1M Git commit messages from the Linux Kernel: [linux-commits-search.typesense.org](https://linux-commits-search.typesense.org/)
- Spellchecker with type-ahead, with 333K English words: [spellcheck.typesense.org](https://spellcheck.typesense.org/)
- An E-Commerce Store Browsing experience: [ecommerce-store.typesense.org](https://ecommerce-store.typesense.org/)
- GeoSearch / Browsing experience: [airbnb-geosearch.typesense.org](https://airbnb-geosearch.typesense.org/)
- Search / Browse xkcd comics by topic: [xkcd-search.typesense.org](https://xkcd-search.typesense.org/)
- Semantic / Hybrid search on 300K HN comments: [hn-comments-search.typesense.org](https://hn-comments-search.typesense.org)

🗣️ 🎥 If you prefer watching videos:

- Here's one where we introduce Typesense and show a walk-through: https://youtu.be/F4mB0x_B1AE?t=144
- Check out Typesense's recent mention during Google I/O Developer Keynote: https://youtu.be/qBkyU1TJKDg?t=2399
- Here's one where one of our community members gives an overview of Typesense and shows you an end-to-end demo: https://www.youtube.com/watch?v=kwtHOkf7Jdg

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

</p>

<p align="center">
 <!-- <a href="https://circleci.com/gh/typesense/typesense"><img src="https://circleci.com/gh/typesense/typesense.svg?style=shield&circle-token=82c53eae44fca30bcf7a86d0b239b1e3e79b212d"></a> -->
 <a href="https://hub.docker.com/r/typesense/typesense/tags"><img src="https://img.shields.io/docker/pulls/typesense/typesense"></a>
  <a href="https://github.com/typesense"><img src="https://img.shields.io/github/stars/typesense/typesense?label=github%20stars&style=flat"></a><br>
  <a href="https://cloud.typesense.org"><img src="https://img.shields.io/badge/searches_per_month_on_typesense_cloud-10 Billion-blue"></a>
<p>
<p align="center">
  <a href="https://typesense.org">Website</a> | 
  <a href="https://typesense.org/docs/">Documentation</a> | 
  <a href="https://typesense.link/roadmap">Roadmap</a> | 
  <a href="https://typesense.link/slack-community">Slack Community</a> | 
  <a href="https://threads.typesense.org/">Community Threads</a> | 
  <a href="https://twitter.com/typesense">Twitter</a>
</p>
<br>
<p align="center">
  <img src="assets/typesense_books_demo.gif?raw=true" alt="Typesense Demo" width="459" />
</p>

✨ Here are a couple of **live demos** that show Typesense in action on large datasets:

- Search a 32M songs dataset from MusicBrainz: [songs-search.typesense.org](https://songs-search.typesense.org/)
- Search a 28M books dataset from OpenLibrary: [books-search.typesense.org](https://books-search.typesense.org/)
- Search a 2M recipe dataset from RecipeNLG: [recipe-search.typesense.org](https://recipe-search.typesense.org/)
- Search 1M Git commit messages from the Linux Kernel: [linux-commits-search.typesense.org](https://linux-commits-search.typesense.org/)
- Spellchecker with type-ahead, with 333K English words: [spellcheck.typesense.org](https://spellcheck.typesense.org/)
- An E-Commerce Store Browsing experience: [ecommerce-store.typesense.org](https://ecommerce-store.typesense.org/)
- GeoSearch / Browsing experience: [airbnb-geosearch.typesense.org](https://airbnb-geosearch.typesense.org/)
- Search / Browse xkcd comics by topic: [xkcd-search.typesense.org](https://xkcd-search.typesense.org/)
- Semantic / Hybrid search on 300K HN comments: [hn-comments-search.typesense.org](https://hn-comments-search.typesense.org)

🗣️ 🎥 If you prefer watching videos:

- Here's one where we introduce Typesense and show a walk-through: https://youtu.be/F4mB0x_B1AE?t=144
- Check out Typesense's recent mention during Google I/O Developer Keynote: https://youtu.be/qBkyU1TJKDg?t=2399
- Here's one where one of our community members gives an overview of Typesense and shows you an end-to-end demo: https://www.youtube.com/watch?v=kwtHOkf7Jdg

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

<a href="https://typesense.link/roadmap">Roadmap</a> | 
  <a href="https://typesense.link/slack-community">Slack Community</a> | 
  <a href="https://threads.typesense.org/">Community Threads</a> | 
  <a href="https://twitter.com/typesense">Twitter</a>
</p>
<br>
<p align="center">
  <img src="assets/typesense_books_demo.gif?raw=true" alt="Typesense Demo" width="459" />
</p>

✨ Here are a couple of **live demos** that show Typesense in action on large datasets:

- Search a 32M songs dataset from MusicBrainz: [songs-search.typesense.org](https://songs-search.typesense.org/)
- Search a 28M books dataset from OpenLibrary: [books-search.typesense.org](https://books-search.typesense.org/)
- Search a 2M recipe dataset from RecipeNLG: [recipe-search.typesense.org](https://recipe-search.typesense.org/)
- Search 1M Git commit messages from the Linux Kernel: [linux-commits-search.typesense.org](https://linux-commits-search.typesense.org/)
- Spellchecker with type-ahead, with 333K English words: [spellcheck.typesense.org](https://spellcheck.typesense.org/)
- An E-Commerce Store Browsing experience: [ecommerce-store.typesense.org](https://ecommerce-store.typesense.org/)
- GeoSearch / Browsing experience: [airbnb-geosearch.typesense.org](https://airbnb-geosearch.typesense.org/)
- Search / Browse xkcd comics by topic: [xkcd-search.typesense.org](https://xkcd-search.typesense.org/)
- Semantic / Hybrid search on 300K HN comments: [hn-comments-search.typesense.org](https://hn-comments-search.typesense.org)

🗣️ 🎥 If you prefer watching videos:

- Here's one where we introduce Typesense and show a walk-through: https://youtu.be/F4mB0x_B1AE?t=144
- Check out Typesense's recent mention during Google I/O Developer Keynote: https://youtu.be/qBkyU1TJKDg?t=2399
- Here's one where one of our community members gives an overview of Typesense and shows you an end-to-end demo: https://www.youtube.com/watch?v=kwtHOkf7Jdg

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | C/C++ / CMake |
| Manifests detected | CMakeLists.txt |
| Files in snapshot | 298 |
| Lines of code | 151843 |
| Dependency references | 4 |
| Dependencies by ecosystem | npm: 4 |
| Upstream license | GPL-3.0 |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| npm | api_tests | . | api_tests/package.json |
| npm | zod | ^3.25.67 | api_tests/package.json |
| npm | @types/bun | latest | api_tests/package.json |
| npm | typescript | ^5 | api_tests/package.json |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

who have the bandwidth to get it production-ready, regularly monitor it and scale it, especially when they have a need to store 
billions of documents and petabytes of data (eg: logs).

Typesense is built specifically for decreasing the "time to market" for a delightful search experience. It's a light-weight
yet powerful & scaleable alternative that focuses on Developer Happiness and Experience with a clean well-documented API, clear semantics 
and smart defaults so it just works well out-of-the-box, without you having to turn many knobs.

Elasticsearch also runs on the JVM, which by itself can be quite an effort to tune to run optimally. Typesense, on the other hand, 
is a single light-weight self-contained native binary, so it's simple to setup and operate.

See a side-by-side feature comparison [here](https://typesense.org/typesense-vs-algolia-vs-elasticsearch-vs-meilisearch/).

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

We are a small bootstrapped team that's trying to do big things with Typesense, so we'd be delighted to take all the help we can get.

Here are a couple of things we're looking for help with:

## ⚙️ Client libraries in additional languages

There are quite a few programming languages out there and we're not experts in all of them. So we'd appreciate your help in contributing towards a client library in a programming language that's your area of expertise. Please join our Slack Community to collaborate on the architecture. 

## 🚉 Integrations with platforms you use

If you use a particular Content Management Framework/System or E-Commerce Framework/Platform, an integration that pushes data from that platform/framework into Typesense would be a great value add for others in the community. 

## 🐛 Feature Requests & Bug Reports

If you find a bug or a missing feature that you'd find useful, please open an issue on Github. 

## 📖 Tutorials

Share your experience with the community about how you integrated with Typesense by writing an article about it. Or write a How-To or Tutorial on how to use Typesense for specific use cases and let us know. We'd love to share your work with the rest of the community by including it in our docs.

## 🏆 Showcases

Want to show-off your work that uses Typesense? We're building a Showcase to collect interesting use-cases for Typesense. Edit [this file](https://github.com/typesense/typesense/blob/master/SHOWCASE.md) and send us a PR.

## 🌟 Spread the Word

We are on a mission to democratize search by building an easy-to-use, yet powerful search engine for everyone. If you know friends, teams or communities that might find Typesense useful, let them know! Also, we wouldn't complain if you starred our Github project :)

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: GPL-3.0** (evidence: `LICENSE.txt` in the upstream snapshot).

License file excerpt:

```text
                    GNU GENERAL PUBLIC LICENSE
                       Version 3, 29 June 2007

 Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

                            Preamble

  The GNU General Public License is a free, copyleft license for
software and other kinds of works.

  The licenses for most software and other practical works are designed
to take away your freedom to share and change the works.  By contrast,
the GNU General Public License is intended to guarantee your freedom to
share and change all versions of a program--to make sure it remains free
software for all its users.  We, the Free Software Foundation, use the
GNU General Public License for most of our software; it applies also to
any other work released this way by its authors.  You can apply it to
your programs, too.
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original GPL-3.0 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `GPL-3.0` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `TYPESENSE` (category: SEARCH ENGINES)
- **Upstream URL:** https://github.com/typesense/typesense.git
- **Pinned commit (SHA):** `82c53eae44fca30bcf7a86d0b239b1e3e79b212d`
- **Branch:** v31
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`d8d253895c447a2c8efb7e7f6e2a81f1fdbcf173a8673b2d97b1b7c610a36c77`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

