# Repolex Knowledge Graph of jaraco/jaraco.path

RDF knowledge graph data for [jaraco/jaraco.path](https://github.com/jaraco/jaraco.path), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download jaraco/jaraco.path
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   ├── 4e85f28b8b03fcad8ef7d78d074b6fd60c59cff2
│   │   │   └── chunk-001.nq.gz
│   │   └── ec200227226108abdd943d2264360619b9d35ddc
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── ec200227226108abdd943d2264360619b9d35ddc.nq.gz
│   └── repolex
│       ├── 4e85f28b8b03fcad8ef7d78d074b6fd60c59cff2
│       │   └── chunk-001.nq.gz
│       └── ec200227226108abdd943d2264360619b9d35ddc
│           └── chunk-001.nq.gz
├── blob
│   ├── 01f0975f5cb88efd24ae85034fd80488916fd525.nq.gz
│   ├── 13ccecf3b605417aa4b30211c7bf17d8cdb06160.nq.gz
│   ├── 1bb5a44356f00884a71ceeefd24ded6caaba2418.nq.gz
│   ├── 1e8311543c909f9ac2a14d5e80407697e5360b0f.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 2721872abbe586b31147268904eb6099135183ca.nq.gz
│   ├── 2c5499130acc293d5eaebc76ecd0a48bd537b2b9.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 57a7cdce900e978e8746d684fa0b04c4e65f9c4a.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 5c05f9e27d57a4b7a3c3a9fdfecf8cddb8be499f.nq.gz
│   ├── 6fa480e44f38768722368d7a986607adacf41d99.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 83b0d15c6b61a31860b993d152db2adc7dd120f0.nq.gz
│   ├── 89ff33961ba3d6f9cda89322a1fdbf1ac2e35513.nq.gz
│   ├── 8ec58e22fa608ebd943278a4b28b15c090ac722e.nq.gz
│   ├── 922aa1f19856d5841e80b0a2370e0e5fa7c41512.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── a28d0624a7ae1a9ef4193207d45b3f6e8a31c2d1.nq.gz
│   ├── ac0ff69e22507b430cfb9a91d98e2451a3de52d9.nq.gz
│   ├── afc781a3a40064aa0f5c493643446250e3ebaf5d.nq.gz
│   ├── cbab22662278c38214c715caa1a4f875f7bbca1a.nq.gz
│   ├── dc8516ac20b3d38cf754fe8d804ffdffafc15ef0.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e370b52c550d6f315b59268ec792dd0ffca77b75.nq.gz
│   ├── efcb8cbc2043faa7caf4f92fc7488bd6914c934c.nq.gz
│   ├── f1fa5fbdcd0a2e63a8ecc73165c05bbf2fe70845.nq.gz
│   └── febf79524d701fc101f47561a1762654e92771b4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── ec200227226108abdd943d2264360619b9d35ddc.nq.gz
├── filetree
│   ├── 4e85f28b8b03fcad8ef7d78d074b6fd60c59cff2.nq.gz
│   └── ec200227226108abdd943d2264360619b9d35ddc.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

17 directories, 46 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[jaraco/jaraco.path](https://github.com/jaraco/jaraco.path)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
