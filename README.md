# Repolex Knowledge Graph of saghul/aiodns

RDF knowledge graph data for [saghul/aiodns](https://github.com/saghul/aiodns), parsed by [repolex](https://repolex.ai).

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
rlex download saghul/aiodns
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ff43a83ea57e195e56af73b9bafe6a9dbc2d6e18
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ff43a83ea57e195e56af73b9bafe6a9dbc2d6e18
│           └── chunk-001.nq.gz
├── blob
│   ├── 04a5f752b97e2f7e429fdcf402ed810932812f96.nq.gz
│   ├── 052152dd8f4bf0afd83d6896d53deeae58ab15ee.nq.gz
│   ├── 1b5d7a0de70c3c532cfc59fffdf97511f7d0bb92.nq.gz
│   ├── 1fed03cb713713400735dfbd3f99b869021059d7.nq.gz
│   ├── 20203fa6793fefc855c730a6fa8557e97e79eda1.nq.gz
│   ├── 295dd463786d5b1e8d759450a0b9f83f5cd52c80.nq.gz
│   ├── 36979982708b367032730848375b2a457cf360b8.nq.gz
│   ├── 3fac3f1fcd85ffa90e753c8b3a88083bac29b272.nq.gz
│   ├── 412a8a0aa0a7764f7f5c94c87290aef2df7c4e53.nq.gz
│   ├── 4a573e3a4cf00485c601db074f78c7785b5e61e2.nq.gz
│   ├── 5af7c8c319048c0059d4962f8f3d8e147752efd2.nq.gz
│   ├── 600d62b22d82407002aa9a615f134c5a833ad011.nq.gz
│   ├── 64daa0504b48b5336c22f5ecc54547e766bea1fc.nq.gz
│   ├── 7497f5f9111685cd5e144124e34f5897e9c1bcfe.nq.gz
│   ├── 82355eaad60858af78edcd50281e01f4dd0f4a1a.nq.gz
│   ├── 82af0d475b1f3b982d5eb8ad9999e8b7a6ba8978.nq.gz
│   ├── 9bbc4e013aa5db5d91af3dea28d5a4a65c67f5a0.nq.gz
│   ├── a055674ca4b8e9665cb58419ce329778ade7eec6.nq.gz
│   ├── a2c76437f388028f5d337f13900e1ff46589c775.nq.gz
│   ├── a2ebfc88bdd97a50ec8d2f640fceec27fdfc2230.nq.gz
│   ├── af57bc0b387f305a40c265731ba8580c3b050d05.nq.gz
│   ├── b2f4db578b4c4677aae0e08fb98e33b3645cf203.nq.gz
│   ├── b9fb8a6e0f4a5ce99899eb97d872c6b90f4bb678.nq.gz
│   ├── c166434db501cc9737abed55a3d51dd833f04645.nq.gz
│   ├── cb06b36d91edaf5c0a31aa61d590805b837960ce.nq.gz
│   ├── d75e91fe2eaf39b000abae9cf39373f4529b409c.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ff43a83ea57e195e56af73b9bafe6a9dbc2d6e18.nq.gz
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

[saghul/aiodns](https://github.com/saghul/aiodns)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
