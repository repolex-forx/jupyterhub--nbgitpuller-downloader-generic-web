# Repolex Knowledge Graph of jupyterhub/nbgitpuller-downloader-generic-web

RDF knowledge graph data for [jupyterhub/nbgitpuller-downloader-generic-web](https://github.com/jupyterhub/nbgitpuller-downloader-generic-web), parsed by [repolex](https://repolex.ai).

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
rlex download jupyterhub/nbgitpuller-downloader-generic-web
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3d6080c92a610d72f02bf1d15a65fbf15b625604
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3d6080c92a610d72f02bf1d15a65fbf15b625604
│           └── chunk-001.nq.gz
├── blob
│   ├── 07de284aa5c45f56b69ca6f605edf72a14785b99.nq.gz
│   ├── 38622c14099996a920c3438fb3022ef168672ac9.nq.gz
│   ├── 5025ce4e109c0024928f2910db710a81362a5baa.nq.gz
│   ├── 55e86c7aa34ae6e460cd28b472fbe8d0b07df70a.nq.gz
│   ├── 569745928e70ddc4e0ac352d2bab6e8a633cb8fe.nq.gz
│   ├── 7c7a753cbabba685dc3e67f1236dcdad2cc055ab.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f321722a6c519ddcf10c62f71324fa36741380e6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3d6080c92a610d72f02bf1d15a65fbf15b625604.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 15 files
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

[jupyterhub/nbgitpuller-downloader-generic-web](https://github.com/jupyterhub/nbgitpuller-downloader-generic-web)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
