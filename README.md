# Repolex Knowledge Graph of pylint-dev/pylint-plugin-utils

RDF knowledge graph data for [pylint-dev/pylint-plugin-utils](https://github.com/pylint-dev/pylint-plugin-utils), parsed by [repolex](https://repolex.ai).

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
rlex download pylint-dev/pylint-plugin-utils
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cee16e5e91101beb10c57b52d80f202eb0c52f40
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cee16e5e91101beb10c57b52d80f202eb0c52f40
│           └── chunk-001.nq.gz
├── blob
│   ├── 0bc6aaba70b550daec21af700ea236322b81cb0b.nq.gz
│   ├── 2473010a85e274c21b0ec899e1451791a52172a8.nq.gz
│   ├── 2f8df88e739d9c245830abfdf018a0fcbdcfca4b.nq.gz
│   ├── 3cb90f7626a61af6edb55adb10b7de36e309e35c.nq.gz
│   ├── 3d2a6a0ec6295d3b9af00e000bb536b31217bc6b.nq.gz
│   ├── 768e42dce60f2f8ecf9626c951ed2d79f6630dba.nq.gz
│   ├── 90674f0989c45fa64be6cc0636c256429213da09.nq.gz
│   ├── 918c8a27ceb1d3d439cdd729190d1c83dbdd8060.nq.gz
│   ├── aa9d3be300372edbe3b50070cd3559ce22c3adc9.nq.gz
│   ├── ad67b32c42aab644fbb03b084d56b1193b0fed12.nq.gz
│   ├── b90ab14859e95c8381efd6a41a4060bfb6fec101.nq.gz
│   ├── bd65411565f9c6d6e2fca85258df1660751f2a9d.nq.gz
│   ├── c804e1b1c61a14ad82ef80bf73197af9b1f44f97.nq.gz
│   ├── d847e9c3678401351fc88822ffc62f4dad74ac20.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cee16e5e91101beb10c57b52d80f202eb0c52f40.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 23 files
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

[pylint-dev/pylint-plugin-utils](https://github.com/pylint-dev/pylint-plugin-utils)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
