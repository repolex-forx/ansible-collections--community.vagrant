# Repolex Knowledge Graph of ansible-collections/community.vagrant

RDF knowledge graph data for [ansible-collections/community.vagrant](https://github.com/ansible-collections/community.vagrant), parsed by [repolex](https://repolex.ai).

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
rlex download ansible-collections/community.vagrant
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 84af372cc0b2d4c8a339cb720257d4f5cadd681e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 84af372cc0b2d4c8a339cb720257d4f5cadd681e
│           └── chunk-001.nq.gz
├── blob
│   ├── 00760a739dc40099137f8bfdcc79b668e54019da.nq.gz
│   ├── 0164155b81025416095f31a4732098ec238e6476.nq.gz
│   ├── 01b97249ab313360c173e10a3338c73281cc623d.nq.gz
│   ├── 01d3427b6a2ee225d9818bb1268d17ae913632ee.nq.gz
│   ├── 0cc98db2227faec417d422ccfdc1ac424447b81b.nq.gz
│   ├── 108025888ef1ffbc86575aa0f1bcf79a60c50b46.nq.gz
│   ├── 17fc011035d1bd4cbcd4daad1040de91fa26faa6.nq.gz
│   ├── 1d3dc5ac6e8cfacab31aae4dae3c335dfcfa3d61.nq.gz
│   ├── 44f6d372cc5d34dc88891927eec4afdf7827ceeb.nq.gz
│   ├── 4f6f7157ff8f2e5266373a240e64b3d6f71d02a2.nq.gz
│   ├── 50f0e6c357fee7cb93c847089153e11b483c4519.nq.gz
│   ├── 56ae93356cd245b01d3d14c18edb95522ef77ab8.nq.gz
│   ├── 5acc2a4a9f79333c2389fd4fddafeb7d05cf1527.nq.gz
│   ├── 740c8115458b12e3a8f24220e718e0b33ef2e16d.nq.gz
│   ├── 7612a85a4ef2d459df15e003f42921cb38e7309b.nq.gz
│   ├── 7bba0c81374a9a30d0719db51f97ccb95b77068f.nq.gz
│   ├── 7f7afbf3bf54b346092be6a72070fcbd305ead1e.nq.gz
│   ├── 81064c59ccbf1b68609c08a99db85274132f17e2.nq.gz
│   ├── 9005366fb41dc6efd2108ba7402f9789bcb149a1.nq.gz
│   ├── 953744730acf24ff87f44c3413a8ac9f2f18993b.nq.gz
│   ├── 9cd26302315c84ab60e0756bc2477f48782f73c1.nq.gz
│   ├── 9fad0d343c07aa82e21752481014bb870092c693.nq.gz
│   ├── a056a90e5819e018af1cf914f42fb88a8e819c11.nq.gz
│   ├── a764a086fa33a5c5b7f12e092ab7fe9a71d79b03.nq.gz
│   ├── b371112868370b5bf54482058e58a2cae8ba8c59.nq.gz
│   ├── c854e93832215825f9eebd763b749b451cc90c71.nq.gz
│   ├── c89949397703c3c627f4c70d0974f04ac4ba032e.nq.gz
│   ├── d14ac0e656be099ab33c10d4ceab46baab70f654.nq.gz
│   ├── d2e1af8830b03f5a1720f62735f1b979b921e5c8.nq.gz
│   ├── d354e2ce6f6f9bc8a671fdf5bb1d360ac516505a.nq.gz
│   ├── d6d7deb569d76225c0f35efbc687bf970fd34439.nq.gz
│   ├── d8c1b97b765848349cc99290385320a570e17c1d.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ee377cdbcf0aa0a5989dc68994628fbf20ceefee.nq.gz
│   ├── fafcb3eb56407e6add7a69c455e3db7aff590e59.nq.gz
│   └── fbc6f9f5c0ef8dd74c977c5d86d0aed03f41a48a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 84af372cc0b2d4c8a339cb720257d4f5cadd681e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 44 files
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

[ansible-collections/community.vagrant](https://github.com/ansible-collections/community.vagrant)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
