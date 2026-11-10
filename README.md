# Repolex Knowledge Graph of mattn/go-colorable

RDF knowledge graph data for [mattn/go-colorable](https://github.com/mattn/go-colorable), parsed by [repolex](https://repolex.ai).

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
rlex download mattn/go-colorable
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 56c5db567780daeef4a4ffbb2c14d7d4b6b94b9b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 56c5db567780daeef4a4ffbb2c14d7d4b6b94b9b
│           └── chunk-001.nq.gz
├── blob
│   ├── 012162b077c97e96bcb25c4be1a0716a29a35fd6.nq.gz
│   ├── 054d92be57ccd17d2af29184ab79ea17e44c8b97.nq.gz
│   ├── 1d7f7530d696ad5e84b24b57957bf4ea5d0bbfeb.nq.gz
│   ├── 24da3db485cee5b8c1252ec2c837270343325252.nq.gz
│   ├── 2602177d54b1f5a606d8f9b5c7762bfe3f2e88b2.nq.gz
│   ├── 2af32bd60fa05aea24535d8e408fba26df076854.nq.gz
│   ├── 2e1f1ab1adc802be1169a34b20f646842b209345.nq.gz
│   ├── 349b0a8205f59490c9f88c4795a57c9fba33b749.nq.gz
│   ├── 351ae11a875b1ac5c17b74b247b8a7c3c4716796.nq.gz
│   ├── 4ddd5a7cc8929a17601bc9fe738daff33fe70415.nq.gz
│   ├── 55798acb17c41a64c02ee7495f147a752da55c2e.nq.gz
│   ├── 5fc3c567a8dbf0a204ec694c6911ab8755ee46ff.nq.gz
│   ├── 87904774c163f1bc553fc440af962e5b88742443.nq.gz
│   ├── 8931ebb6e66059999c950865573e2986e4cf9774.nq.gz
│   ├── 8cbcb909760e7797d92d896255aebee3c78f7ca8.nq.gz
│   ├── 8f0430eab1731ad012a326e0db08c6cfa09ca962.nq.gz
│   ├── 91b5cef30ebdf08cb6efe669497a96f58c66035d.nq.gz
│   ├── 92261f8e306fb23ad6164875be893977e9e30754.nq.gz
│   ├── 961feae654111f001a73f5a6a1b369a64fd5d79c.nq.gz
│   ├── 97ac5d7523395ef1f91c34f76921343862780fa5.nq.gz
│   ├── afc88e7431729c47eca15e29d6555cb94c2e10b2.nq.gz
│   ├── c0abba1ed9d6c46815c721a107b2df902dec7704.nq.gz
│   ├── c1a78aa94d08c0547608b28b4c915a45c22533af.nq.gz
│   ├── c569164b2e2b074d1ff2eeef0aa07d7c5186bf18.nq.gz
│   ├── ca0483711c93d6f536dffafcf69579adcaff6882.nq.gz
│   ├── f380a801f71b52387ead62c6da53c6ff5ba76122.nq.gz
│   └── f451d5347a3b6553b586aefb261b31ae81aea7b8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 56c5db567780daeef4a4ffbb2c14d7d4b6b94b9b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 35 files
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

[mattn/go-colorable](https://github.com/mattn/go-colorable)

---
*Parsed on 2026-11-10 by [repolex](https://repolex.ai)*
