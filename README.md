# Repolex Knowledge Graph of pytest-dev/pytest-twisted

RDF knowledge graph data for [pytest-dev/pytest-twisted](https://github.com/pytest-dev/pytest-twisted), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-twisted
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 90343f7b116220228233108a0fafaefecf34140e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 90343f7b116220228233108a0fafaefecf34140e
│           └── chunk-001.nq.gz
├── blob
│   ├── 0b3e79f027585650088da139b20e085945014e8e.nq.gz
│   ├── 23d383006a80a0090eafdc40352f8f39965b8d01.nq.gz
│   ├── 279ab419fbe16a30e100ed75180d9af7a73a9e01.nq.gz
│   ├── 294cf7477e541983dd1ea4bf36488eb45fe39bf6.nq.gz
│   ├── 558bb2bb61bbc8b76db4bc8b8add54c9e3d31391.nq.gz
│   ├── 5636cda2a90d81538d0ce5cb0534a8786375888e.nq.gz
│   ├── 69f9baa944ec4c6f0f10adb2fdb24e1d0ae30b87.nq.gz
│   ├── 73f131890869b28e7e31b3d3a34ca91e327d2032.nq.gz
│   ├── 7f1532e1b0e0c82bc2859a27b4b464e75e1e2055.nq.gz
│   ├── 9050191141bdcd30d918c043d81f11e9c99b988b.nq.gz
│   ├── 9885b491f17e9c7af901cbc9623032766164fd8f.nq.gz
│   ├── b0c4d97ef670a679eaf975b90baa7e532fcfb555.nq.gz
│   ├── c3234491567dee550e6dbdd8a5b7ccbeace63827.nq.gz
│   ├── c341da54fc384472204ef950c72e67ff5131123a.nq.gz
│   ├── c8ed3b72bc5050534beca0213bd35e2692f4d811.nq.gz
│   ├── dacab70c368d11817b883f640e7d13fad15983f1.nq.gz
│   ├── e11ea6d4c1c095db878ebf68f8f0114b7fc1c90e.nq.gz
│   ├── e8ce955058f484820f076062081ce8a8e897b32b.nq.gz
│   ├── f6497ecad59b43520e4d3c7b6629162e574b5e4d.nq.gz
│   └── f9e1ce87bef6c08fccc30a0cc2503257d2c75a13.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 90343f7b116220228233108a0fafaefecf34140e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 28 files
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

[pytest-dev/pytest-twisted](https://github.com/pytest-dev/pytest-twisted)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
