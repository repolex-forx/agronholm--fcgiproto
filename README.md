# Repolex Knowledge Graph of agronholm/fcgiproto

RDF knowledge graph data for [agronholm/fcgiproto](https://github.com/agronholm/fcgiproto), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/fcgiproto
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6dd4cc23661d84a4aaf9aa208202a44710ff60a5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6dd4cc23661d84a4aaf9aa208202a44710ff60a5
│           └── chunk-001.nq.gz
├── blob
│   ├── 02b0c4cf2ef4768eadd3f531fe2daea957ad3689.nq.gz
│   ├── 067698fa627e6669579f4ca32be31fe3f95c98fd.nq.gz
│   ├── 07806f8af9dd3253ebdb5710b67e73124aea4941.nq.gz
│   ├── 1271d09caa56e009142dab74a47ae57c48c70536.nq.gz
│   ├── 170b1f721a3ef801b19f82cefa68221937138310.nq.gz
│   ├── 1961da705fd74a4f104ba8355b1136b7ea0eb10f.nq.gz
│   ├── 23c69634a9584f8b2e24f59474b3965eeba7641c.nq.gz
│   ├── 2f0bb2b1f58e522fac7b5ffd9e2f57597d076449.nq.gz
│   ├── 340b3452b60d3f284f9ec6f1c9f01bd518b35042.nq.gz
│   ├── 39f25d8a162c1775b8a2bd155c6ca888e3716d86.nq.gz
│   ├── 3f3f45c058a152d6cf3f15af6e9eae20d5047146.nq.gz
│   ├── 492bc5ed012e876b28584e09efe77e589af1997c.nq.gz
│   ├── 69d4ae52fab6cfa4f9d27e6029bd604aeca92eb9.nq.gz
│   ├── 6d41d51946cbdb01ecd586416156f2ed4bfe4e3e.nq.gz
│   ├── 6f182eb24a67c0a2d358d60193a546b61d06ae25.nq.gz
│   ├── 85d336d962b73810ddaa08cd092a172c732c052f.nq.gz
│   ├── 8cdb39694467adc45921a9f51c5bd42d83a63eb8.nq.gz
│   ├── 8f02729ef34ba1a71f1c37c8bf7362407e640416.nq.gz
│   ├── 98e2f463cad0adb29be396535933f186ee090dab.nq.gz
│   ├── a11615e6dc65244dcdb2e96efd8bf60fc1a77d72.nq.gz
│   ├── b44e1bb5ee679a7facd34bdec006a5fa2be1b4db.nq.gz
│   ├── b7e8f90c009625864973005c84155e22f1506dc4.nq.gz
│   ├── bc99f713d518571ff59778b1b1c2cf6810bf3812.nq.gz
│   ├── c36dce090ff988c8b48b03740c4ffd36f595bb6b.nq.gz
│   ├── d9654a90f6c8015b00dcbe0cc6fe8f437fb17cd7.nq.gz
│   ├── e2ee148f6cecb9d5c0a5d9652e938213efa893cd.nq.gz
│   ├── ead6ad5f6102e67596ea926559393655a06e6dab.nq.gz
│   ├── eeefa641c30d896425e22f29726025f6e5b8149e.nq.gz
│   ├── f1dd5b66a1f24576dd54b83965b057a19281b669.nq.gz
│   ├── f8097b581d142d8d262ce805b2dabf1d28e82a1e.nq.gz
│   └── fd86bd5eabe752700b7c44a18ae39c700b6e64bc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6dd4cc23661d84a4aaf9aa208202a44710ff60a5.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 38 files
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

[agronholm/fcgiproto](https://github.com/agronholm/fcgiproto)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
