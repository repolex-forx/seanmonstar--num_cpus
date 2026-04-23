# Repolex Knowledge Graph of seanmonstar/num_cpus

RDF knowledge graph data for [seanmonstar/num_cpus](https://github.com/seanmonstar/num_cpus), parsed by [repolex](https://repolex.ai).

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
lexq download seanmonstar/num_cpus
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 342af76b486335e5a955c7314fc96cd104e7a17b
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 342af76b486335e5a955c7314fc96cd104e7a17b.nq.gz
│   └── repolex
│       └── 342af76b486335e5a955c7314fc96cd104e7a17b
│           └── chunk-001.nq.gz
├── blob
│   ├── 022f514ba121a5f357d0590f4751ece848012c6a.nq.gz
│   ├── 041cfaf1eb6926c4f7c2e0a2b6cffa720cff9a09.nq.gz
│   ├── 16e37df1d1b6b60305c74dcd97d9b3289f73063e.nq.gz
│   ├── 16fe87b06e802f094b3fbb0894b137bca2b16ef1.nq.gz
│   ├── 1a9282a6e41cfdff6b280ea9bfc0c5c1c598560f.nq.gz
│   ├── 24e757f51c35718afa8e0ff6cba233a44be18b88.nq.gz
│   ├── 26f3b3ddf286f4d90b3fd16585d4edaee0f74197.nq.gz
│   ├── 295c925fbab13dd39ba738b4ea7fc8d20ec1f5d4.nq.gz
│   ├── 3583b3e76e25563c8426df9b3f4a9d733b1632c0.nq.gz
│   ├── 35b49db2c08ca19859102027ff1756559b8fd054.nq.gz
│   ├── 36ee2b825ba626622a345ecedff5c6f1cdbd3000.nq.gz
│   ├── 37f4e25359f2bfcebf61be1216bcb8f966583cd1.nq.gz
│   ├── 5685b08c6740b4d72632440e0ee6fb4576a0c1af.nq.gz
│   ├── 5e854c5fbb45ba8ad407446c71b755b1077270d9.nq.gz
│   ├── 74041b8de09978475148bcc0b4767ad791a6f738.nq.gz
│   ├── 7636a477bf48ba32ea007429ccb429ae8d6ee0ec.nq.gz
│   ├── 77ac542d4fbf044fb1ea10086971de8ad97f8603.nq.gz
│   ├── 7b23b57a60f11336012f3f70d13afc2da8df0348.nq.gz
│   ├── 833a8f2d3b677f5be80c6e7c87bb2de860a659ce.nq.gz
│   ├── 9954063dcc7bb76719c38446fd41057fc968a5cd.nq.gz
│   ├── a47f047247f2b44479440409ed231d8212e6bacf.nq.gz
│   ├── a9d37c560c6ab8d4afbf47eda643e8c42e857716.nq.gz
│   ├── ad27a964f3aa6ca6ac6377e96391b5aae12261c7.nq.gz
│   ├── cb2bf3ec7a23e6b0f94b59ac092ad9cce2215afe.nq.gz
│   ├── da36e4102ff5135d2e1ba48b66ed1f366eff5a79.nq.gz
│   ├── e03a95b42597a5a0b68d911f87f320324ed7a5d3.nq.gz
│   ├── e469067a61a198cb50826deed50cf1da5dcd8509.nq.gz
│   └── f85a1376c6ba75a05c5f12fda491c2d7b3dc7a6e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 342af76b486335e5a955c7314fc96cd104e7a17b.nq.gz
├── filetree
│   └── 342af76b486335e5a955c7314fc96cd104e7a17b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 38 files
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

[seanmonstar/num_cpus](https://github.com/seanmonstar/num_cpus)

---
*Parsed on 2026-04-23 by [repolex](https://repolex.ai)*
