# Repolex Knowledge Graph of dateutil/deadsnakes-action

RDF knowledge graph data for [dateutil/deadsnakes-action](https://github.com/dateutil/deadsnakes-action), parsed by [repolex](https://repolex.ai).

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
rlex download dateutil/deadsnakes-action
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── dafca658ce5a39e29d3f1d1da2d9a343c1f9ce9e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── dafca658ce5a39e29d3f1d1da2d9a343c1f9ce9e
│           └── chunk-001.nq.gz
├── blob
│   ├── 0eea44b41ca30a28f89da7ab18b0398a44333aad.nq.gz
│   ├── 6db4cf4150997b00ef3aa5c030f8d0fb93a8d532.nq.gz
│   ├── 7f2b679709107924bee6470c4ea92d3712cc891d.nq.gz
│   ├── 9137f742a666cb559217bc0d37379671d27d45aa.nq.gz
│   ├── b6c2693071afdfc05b396e4c087145783ad3d0d7.nq.gz
│   └── ebf77671f66017d72f2b472c15ba09427ed831c1.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── dafca658ce5a39e29d3f1d1da2d9a343c1f9ce9e.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 12 files
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

[dateutil/deadsnakes-action](https://github.com/dateutil/deadsnakes-action)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
