# Repolex Knowledge Graph of block/bitcoin-augur-reference

RDF knowledge graph data for [block/bitcoin-augur-reference](https://github.com/block/bitcoin-augur-reference), parsed by [repolex](https://repolex.ai).

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
rlex download block/bitcoin-augur-reference
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── af31e0e941ff5dfca0443e465989727f1dba90b6
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── af31e0e941ff5dfca0443e465989727f1dba90b6.nq.gz
│   └── repolex
│       └── af31e0e941ff5dfca0443e465989727f1dba90b6
│           └── chunk-001.nq.gz
├── blob
│   ├── 0367d2331a2cbfb3dadb43da08affe106a235c28.nq.gz
│   ├── 081cbe83449cf8e625a3e2e79b6b35415c4e1503.nq.gz
│   ├── 11bea106ecdd7882fc6a5d5dbfe537ddf66bf565.nq.gz
│   ├── 197a03fe4890f605e2d8bbee139406e4cb03fc9e.nq.gz
│   ├── 198462b00f3cdaaf58aa8bd2313cceb8d9f4a510.nq.gz
│   ├── 1a1df48e2ad1da7698039e48d2e3862e8ae629a7.nq.gz
│   ├── 21896d558c7c86873f75fd2f9be745c4a83995a1.nq.gz
│   ├── 27461f0699cda61900a43ec4c9c8a57d055dcd60.nq.gz
│   ├── 31559b7d115e3c105b328cce9b9dcd9774025061.nq.gz
│   ├── 315f3a3f76c13b83c2aa04269e32939b7cdc9dc7.nq.gz
│   ├── 335bbddacbf347ff460c1a0d5cf14cdc38b57c37.nq.gz
│   ├── 377538c9965c6177781d5bbf1fdc2644e77d7950.nq.gz
│   ├── 383f4511d444516caed0fd113ee8a2b640cd2290.nq.gz
│   ├── 3a2488bdc75b20ed39b5545016e0d78754aa04b2.nq.gz
│   ├── 3c8fea19ae45c429b691202b5a45221f2372cab5.nq.gz
│   ├── 460b8d142f536bf3b4eca0821f73b31fd93f82f8.nq.gz
│   ├── 5a92c1448559fadf08b8c3c072d1873e62054fbe.nq.gz
│   ├── 796edeb82d9f9ee493758df8d831e80e7650804f.nq.gz
│   ├── 83637a37c33076839f89cb3e315fadbb0101a5d9.nq.gz
│   ├── 83cb96c65994e9ebeb22d6b349a50860b3236aab.nq.gz
│   ├── 9d8c6c4ef1ce482de8b0aa0f709135d441ae2c3b.nq.gz
│   ├── 9fa2049ce2263038bdd4b54f12d253f63788c409.nq.gz
│   ├── a051b8661bd10db68121cb199f8b38c0476a31ae.nq.gz
│   ├── a4b76b9530d66f5e68d973ea569d8e19de379189.nq.gz
│   ├── a61937fc0593b276cdba71aa2bf9970657ec5d32.nq.gz
│   ├── a7a24542082ae2221f09fd1f13f0344c72274ed1.nq.gz
│   ├── ab14ba315330cfc358898b59307056930024ca51.nq.gz
│   ├── b3b0d267f82f062d1f68b2df845d95b67c581443.nq.gz
│   ├── b8669116ff1ab7fe26d95d2ff5834cd7ed597c1e.nq.gz
│   ├── c64c0b8593bddb013948f21e4c2cd390df666204.nq.gz
│   ├── c7afd2b34884d7484cb3ff50aa98f3fcc861f18e.nq.gz
│   ├── cf7b7e07ba8e871e43c99c72a6b0c344d55f1927.nq.gz
│   ├── e2847c820046b34569292608a035c8ffc83be95a.nq.gz
│   ├── e659d59ab2450a05502d07600e55caf144724595.nq.gz
│   ├── e889550ba4cbc92a720527042e5f6e7a303bfcbc.nq.gz
│   ├── f91f64602e6c6d892d70d71f4fc7a1bd943e23f3.nq.gz
│   ├── fe28214d3352b0ed40820a4999317694c8b1ef57.nq.gz
│   └── fe3f64be531d6bdc63c5d1a06e505e49608f5341.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── af31e0e941ff5dfca0443e465989727f1dba90b6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 47 files
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

[block/bitcoin-augur-reference](https://github.com/block/bitcoin-augur-reference)

---
*Parsed on 2026-10-02 by [repolex](https://repolex.ai)*
