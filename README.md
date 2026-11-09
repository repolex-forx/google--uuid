# Repolex Knowledge Graph of google/uuid

RDF knowledge graph data for [google/uuid](https://github.com/google/uuid), parsed by [repolex](https://repolex.ai).

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
rlex download google/uuid
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2d3c2a9cc518326daf99a383f07c4d3c44317e4d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2d3c2a9cc518326daf99a383f07c4d3c44317e4d
│           └── chunk-001.nq.gz
├── blob
│   ├── 0cbbcddbd6e81da612534338c786a4e111bc0a04.nq.gz
│   ├── 138397cb69b73f9c7949c0adc8e12039cb735d19.nq.gz
│   ├── 14bd34072b64d2c9cd0491d00454e593af99e1e2.nq.gz
│   ├── 17bbafe0fb6315c88d0c3da29106cc0192feea61.nq.gz
│   ├── 2e02ec06c0121d1c82a8b07275091549f9a0c950.nq.gz
│   ├── 37c0b5f9b868b8e281c6c1a1565160f218df8151.nq.gz
│   ├── 3fec67102ec3b0e6e6bb4898abb2cfc5d06eeefd.nq.gz
│   ├── 463109629eee180e87507373a3e957e72c34f179.nq.gz
│   ├── 46354a4a41031f3c91d6d8d2ce6c3d3732a727c4.nq.gz
│   ├── 4f6c549125afcb12785baee59058dbb6297729d1.nq.gz
│   ├── 5dc68268d900581915a7bfdc1f2be75cd503dd9e.nq.gz
│   ├── 690c09dabef8cbb410065dd64119b8298c891ba5.nq.gz
│   ├── 6c2ab76b1de49b5b4c8b7f9c7a68e9a801f85724.nq.gz
│   ├── 7697802e4d16b255e7ea22a86071cfbe9af6aa39.nq.gz
│   ├── 7ec5ac7ea9090372537f98b6d4a206485b902248.nq.gz
│   ├── 906ecbe7f8e2b89a63836dfb1fdbcb5763c625e3.nq.gz
│   ├── 91a5fa3259b6149cda25f5df5fd5463665c6c803.nq.gz
│   ├── 929b10f9c9d65a28785c54d9ff70452c1b81472a.nq.gz
│   ├── a502fdc515ac9a531558f10a70b32a47615e0c5a.nq.gz
│   ├── b2a0bc8711b3dcab80f2b96050b318b5748cff70.nq.gz
│   ├── b4bb97f6bcd0d78febc158e7396f10353cdef312.nq.gz
│   ├── d3bc00a31b83b71bc3907d2d135fce059588baac.nq.gz
│   ├── d651a2b0619fa44b7f24cdaf731197e6c1023863.nq.gz
│   ├── d78d1caf469561b8d56d713f11ddb43fcc501c0c.nq.gz
│   ├── d7fcbf28651697b00add519d8b4402a5ab46ffc2.nq.gz
│   ├── db2d1ccf7deff28a611f4cf24392f5459a5d3f20.nq.gz
│   ├── dc75ceefca17f2497d1ac8d99d366251924d2189.nq.gz
│   ├── de4bfb1381b51691d734c526837b9d1b30a0b97e.nq.gz
│   ├── e1bcc3c9b7f29ea58ea89b8f4df052052de426a2.nq.gz
│   ├── efa4d42f2b5830e4ab6a2eab46ba622cacb9af92.nq.gz
│   ├── fa820b9d3092b433238026b451eca869387d91fb.nq.gz
│   ├── fc84cd79d4c79a2ad598d6c5285473aa32b34982.nq.gz
│   └── fe0fe8dd20acaed30bf2ef6b21385ebbcb3c8306.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2d3c2a9cc518326daf99a383f07c4d3c44317e4d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
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

[google/uuid](https://github.com/google/uuid)

---
*Parsed on 2026-11-09 by [repolex](https://repolex.ai)*
