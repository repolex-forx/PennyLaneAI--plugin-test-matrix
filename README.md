# Repolex Knowledge Graph of PennyLaneAI/plugin-test-matrix

RDF knowledge graph data for [PennyLaneAI/plugin-test-matrix](https://github.com/PennyLaneAI/plugin-test-matrix), parsed by [repolex](https://repolex.ai).

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
rlex download PennyLaneAI/plugin-test-matrix
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9185332f5ccdc7c7a693bd27231d3b3f0bb18007
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9185332f5ccdc7c7a693bd27231d3b3f0bb18007
│           └── chunk-001.nq.gz
├── blob
│   ├── 032c9378ada4afc1daad84bc14aa768cef3de4cc.nq.gz
│   ├── 05800c368adb9c62b2b04a22128434189c185482.nq.gz
│   ├── 182ae9d6a7f1ac91b79cde1312645ede31aac258.nq.gz
│   ├── 18cd16d3b412fce40335e9b10b41ad305e347467.nq.gz
│   ├── 18d4434247677d9116e6c2c36cc23d5a67de7186.nq.gz
│   ├── 222f067c4869e10200f67afc4db2b12955e6316d.nq.gz
│   ├── 2608271d8b67bd42a6b76507874e5099185ecdcf.nq.gz
│   ├── 34364040a08844e16907025c020ccbbe1eb0dd15.nq.gz
│   ├── 3b689a797ef374a3d657188025c6fd5a02709c05.nq.gz
│   ├── 4308610ac9e417fa73a8927cce2505318313d97b.nq.gz
│   ├── 5008ddfcf53c02e82d7eee2e57c38e5672ef89f6.nq.gz
│   ├── 67dfb89e4a475c8e4ea09db73fc4211ad4eefdb0.nq.gz
│   ├── 89af071c3b8bac18e7529196eae043f5566a0e61.nq.gz
│   ├── 9b422231300448b9cedea188ae6bae879c747eb2.nq.gz
│   ├── 9b434427f81f9032ea0f54158bbc8eba0dd7c3dd.nq.gz
│   ├── 9c476ef08aa33a2d7a292e304a68c8851220f98f.nq.gz
│   ├── 9cdf9ba3cdc8a1425c8d5c899b495d03875a36ee.nq.gz
│   ├── 9dedda5e861ff9b202277b89150090c88b66083d.nq.gz
│   ├── a785654c561f3e22d8dc15648ea122473c74d282.nq.gz
│   ├── ab2ee909f450f7a83144af376d21ad94434d25c9.nq.gz
│   ├── ad24a0231f29691eb3d03e187514c06670f18e36.nq.gz
│   ├── b0bad8a051b007c72218c73bdd2f2019bfc4ca26.nq.gz
│   ├── b8ff64c9fe3d96ed75d9637a442a6d34825c0b42.nq.gz
│   ├── bdc8dd7e1c091c2ca3c9a247b2e5a26c96c65cec.nq.gz
│   ├── c2d3707123cb0cd49f77eb632fb54b041ea6aeeb.nq.gz
│   ├── d9320f0ef668b70eef1ad1f60c56868ce09949d6.nq.gz
│   ├── e3021e4a412b7d4aa7225319a4d61f26f88bc8ac.nq.gz
│   └── f0ed9f6379054f455c5e0c642e78deedd552db3f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9185332f5ccdc7c7a693bd27231d3b3f0bb18007.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 36 files
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

[PennyLaneAI/plugin-test-matrix](https://github.com/PennyLaneAI/plugin-test-matrix)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
