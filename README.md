# Repolex Knowledge Graph of asimov-modules/asimov-xai-module

RDF knowledge graph data for [asimov-modules/asimov-xai-module](https://github.com/asimov-modules/asimov-xai-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-xai-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 52b1f8491ebbebc488c3a556fb600d79ac62f8f5
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 52b1f8491ebbebc488c3a556fb600d79ac62f8f5.nq.gz
│   └── repolex
│       └── 52b1f8491ebbebc488c3a556fb600d79ac62f8f5
│           └── chunk-001.nq.gz
├── blob
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 2fa1e6615858f1692ba61b02018ed13a34fccd03.nq.gz
│   ├── 35069018eacf56db9eae703174d5bdc773d733e8.nq.gz
│   ├── 35df5f41ca1c0a8ea1174d779dad48a2367d3cc7.nq.gz
│   ├── 594b928051d632cb067863ad5f9838dad80cb386.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 74f2bb48d1cd867d2266e0387a23baffba529a0c.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 99899ecb27e308a201d88cd20cb498e1a04ac4ba.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── bcab45af15a0f1b0166daf8cbf18b17cd8649277.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ee975280b27ffd71a7cbe930034bfcf54d737cd8.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 52b1f8491ebbebc488c3a556fb600d79ac62f8f5.nq.gz
├── filetree
│   └── 52b1f8491ebbebc488c3a556fb600d79ac62f8f5.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[asimov-modules/asimov-xai-module](https://github.com/asimov-modules/asimov-xai-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
