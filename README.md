# Repolex Knowledge Graph of tlvince/make-coverage-badge

RDF knowledge graph data for [tlvince/make-coverage-badge](https://github.com/tlvince/make-coverage-badge), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download tlvince/make-coverage-badge
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 678a2f82dab365f0436d514f695a61189e1f6ac7
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 678a2f82dab365f0436d514f695a61189e1f6ac7.nq.gz
│   └── repolex
│       └── 678a2f82dab365f0436d514f695a61189e1f6ac7
│           └── chunk-001.nq.gz
├── blob
│   ├── 015d2e9baf925f8868f6808b75ed6de128bab34f.nq.gz
│   ├── 06de0dd02868d294a6f04d42167ccceff0c32f4b.nq.gz
│   ├── 176a458f94e0ea5272ce67c36bf30b6be9caf623.nq.gz
│   ├── 1fccc0a2ae97c5c915bd9f39ba2dce0b29a62a18.nq.gz
│   ├── 28880c488d370bd1c1db0beb0e7a1e6490e5f084.nq.gz
│   ├── 44f516e9e1dd4fbaa86d93b97cae60d8e201aa88.nq.gz
│   ├── 535ca80dcc5a695e37dd90273110a2a2726c6b0a.nq.gz
│   ├── 60095bc730109aee211d0c120481ca1bb226992a.nq.gz
│   ├── 68f54f33138e63132dfebdbcd25a84e631df62c3.nq.gz
│   ├── 7423a39ab089afc391a6f3f1ea68983e8d4c6278.nq.gz
│   ├── 8089615103844a00aeee8c1f929fafdbccffce0f.nq.gz
│   ├── 8441f8ce02e17289a4ad4ffef3c1e9bda683541f.nq.gz
│   ├── 8a42903ca49abf94d3708cc2d970ecee06e80fcc.nq.gz
│   ├── 9712366087a842633366dc76ba237e9e11ac89b9.nq.gz
│   ├── 9c4e7d71a801cd378786f7e6d8216b380f5b16b9.nq.gz
│   ├── b2f39de61f1a2cdbeaf498ae779d58b128b4d661.nq.gz
│   ├── bb79d656aa5aa3b11308ed415fd22296c1f4e7c4.nq.gz
│   ├── ca4862a424bc3812d2352b94a380178bbe813ee0.nq.gz
│   ├── cffe8cdef132f31903a4971117f33f60cd9a56e6.nq.gz
│   ├── d5e1c33640d071376a4a3ed10484f80186ea2390.nq.gz
│   ├── e717f5eb6387be229227ad8eba6a56f4cd904ade.nq.gz
│   ├── e83dc0b067720670e6e41acb8ef15b2ff3fa78b8.nq.gz
│   ├── ecef624dfd7246d762775b2b3b26e219741d81a0.nq.gz
│   ├── fb81a036dcfdf9c01694230b5ceee94c86b2402e.nq.gz
│   ├── fc3ea0b2cd4358f801fa1a3f95406aa1d76f5070.nq.gz
│   └── fd0b3333925d922bf8d9e0446ff388c19a855227.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 678a2f82dab365f0436d514f695a61189e1f6ac7.nq.gz
├── filetree
│   └── 678a2f82dab365f0436d514f695a61189e1f6ac7.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 36 files
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

## Source repository

[tlvince/make-coverage-badge](https://github.com/tlvince/make-coverage-badge)

---
*Parsed on 2026-04-16 by [repolex](https://repolex.ai)*
