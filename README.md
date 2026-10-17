# Pustaka Terbuka — PSSSLIMS (Pusat Sumber Sekolah Malaysia (SLiMS Engine Gateway))

> **Pustaka Terbuka: Katalog Induk Terbuka untuk Perpustakaan dan Sekolah Malaysia.**  
> *Official Pusat Sumber Sekolah Malaysia (SLiMS Engine Gateway) (PSSSLIMS) Bibliographic Dataset & Standalone Harvester.*

This repository contains the harvested open MARCXML collection and harvester pipeline for **Pusat Sumber Sekolah Malaysia (SLiMS Engine Gateway)** (`PSSSLIMS`), contributing to the national Malaysian union catalog at [pustaka-terbuka/opac](https://github.com/pustaka-terbuka/opac).

---

## Institutional Metadata

| Attribute | Value |
| :--- | :--- |
| **Institution Code** | `pssslims` |
| **Agency Code** | `PSSSLIMS` |
| **Official Name** | Pusat Sumber Sekolah Malaysia (SLiMS Engine Gateway) |
| **Institution Type** | `school` |
| **State / Territory** | Kuala Lumpur |
| **Target End Bib** | 100,000 |
| **OPAC Base URL** | [https://slims.web.id/](https://slims.web.id/) |
| **Subject Focus** | Primary and secondary school curriculum, adolescent fiction, and reference works |

---

## Directory Structure

```text
pssslims/
├── README.md                      # Institutional repository documentation
├── package.json                   # Node.js project specification & scripts
├── harvest/
│   └── inbox/pssslims/             # Sealed MARCXML batch chunks and manifests
│       └── <run-id>-chunk-001/
│           ├── manifest.json      # Chunk SHA-256 manifest & metadata
│           ├── provenance.jsonl   # Record-level attribution and fetch logs
│           └── records/           # Batched MARC21 slim XML files
├── tools/
│   ├── harvesters/pssslims/        # Automated OPAC crawler & XML converter
│   └── lib/                       # Supporting MARCXML and validation utilities
└── tests/
    └── harvester-pssslims.test.js  # Autonomous test suite
```

---

## Usage

```bash
# Install dependencies
npm install

# Test run harvester (10 sample records)
npm run harvest:sample

# Run full collection sweep
npm run harvest:full

# Validate dataset integrity
npm run validate-inbox harvest/inbox/pssslims/<chunk-directory>
```

---

## Attribution & License

Dataset harvested and preserved under open library metadata standards for educational, civic, and cooperative indexing. Attribution: **Pusat Sumber Sekolah Malaysia (SLiMS Engine Gateway) (PSSSLIMS)** & **Pustaka Terbuka**.
