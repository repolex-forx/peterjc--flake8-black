# Repolex Knowledge Graph of peterjc/flake8-black

RDF knowledge graph data for [peterjc/flake8-black](https://github.com/peterjc/flake8-black), parsed by [repolex](https://repolex.ai).

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
rlex download peterjc/flake8-black
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6c93de987ee81d1a53430ad71c1fd75ba0fd1bda
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6c93de987ee81d1a53430ad71c1fd75ba0fd1bda
│           └── chunk-001.nq.gz
├── blob
│   ├── 014f8f28c5276abcd5db2552b7af33b4a3d7f70f.nq.gz
│   ├── 018ac39d3073e2fd1bd3851936383c6feb48ce97.nq.gz
│   ├── 0fb587fbc5786b24b2a7e8e749bc7483b531e5cc.nq.gz
│   ├── 1200253aff6a0d1905f826528d5890dc9bc59b7a.nq.gz
│   ├── 13b1bd8e18a2af76ec533e47bb3ebcf9bf7266aa.nq.gz
│   ├── 2fef874fd5d664e26833fc819b0ebf58e1a84b04.nq.gz
│   ├── 42120c4251760c6f93d3245fba46e17342614d9e.nq.gz
│   ├── 4483bfb2806702af877517120ab0435604ec7f28.nq.gz
│   ├── 4e6e08e24841836f2c92ea848de5bcc8278082d9.nq.gz
│   ├── 55ec8d784c3cfc688c31cb32a4225e5f551937b8.nq.gz
│   ├── 56d1e69d275e3f2b5f20c47208c67f8bfd052615.nq.gz
│   ├── 5bd4be1b720ef0da0bf80777e493f423e9f34728.nq.gz
│   ├── 617e04570f123153012055eaa833407864dd2563.nq.gz
│   ├── 68b9bb6b39259982a717073b519edc101aff981b.nq.gz
│   ├── 719bd0548e39c9ccabd7845dd0026ba07363ac82.nq.gz
│   ├── 7b268b137e48b75d7ea724c2730b5150590994a0.nq.gz
│   ├── 81703109a23c30ade0262ae3ab4e61458d292539.nq.gz
│   ├── 8fe28f522db35e0f2c5d285bc7542d9cd19840ed.nq.gz
│   ├── 92f6fd6b9d3d8b7da97455f8a2680b091886b90a.nq.gz
│   ├── 9d26fbf8e54854a6fc0c0840bc88cb80c2114d07.nq.gz
│   ├── a1db0bcf447e6a69d730fd1c495306b5917b993d.nq.gz
│   ├── ba09e30cd50e890486d97c9a0a736ca84679939c.nq.gz
│   ├── c66c20fc8a3d6e974a2272a3cbbfda5f573c80f5.nq.gz
│   ├── c8a5332630c1cf9ef780f790be5874e9a0cd4f83.nq.gz
│   ├── d03c7219125f0e3cf3c5165364b0cd43ba70d19c.nq.gz
│   ├── da1a51f1777488f183e81a18a93c0e266a4cfe42.nq.gz
│   ├── e3a7918323765113a5fb80e8be25a75360d21ec5.nq.gz
│   ├── e54008a9f5bad13b2be9283ac71d92516b7e2e16.nq.gz
│   ├── ec2266bae8a6bfc9690f0c7f114f7c60b63e640e.nq.gz
│   ├── f2575f59619f558bd3a79539472ca27c00f51f06.nq.gz
│   ├── f460bcfec245b90e621d9ad69f861aebc2d4ca00.nq.gz
│   └── fe79ce02d24ce73c01f53e56c514811d9034356a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6c93de987ee81d1a53430ad71c1fd75ba0fd1bda.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[peterjc/flake8-black](https://github.com/peterjc/flake8-black)

---
*Parsed on 2026-10-19 by [repolex](https://repolex.ai)*
