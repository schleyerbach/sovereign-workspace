sovereign-workspace/
├── README.md
├── CHANGELOG.md
├── LICENSE                 # optional, später
├── .gitignore
│
├── docs/
│   ├── governance.md       # Prinzipien & Rahmen (v0.1)
│   ├── roadmap.md          # High-level Roadmap
│   │
│   ├── 01-architecture/    # versionierte Architektur-Beschreibungen
│   │   └── v0.1.md         # (optional: Überblick, später ausbaubar)
│   │
│   ├── 02-adrs/            # Architecture Decision Records
│   │   ├── ADR-0000-public-reference-repo.md
│   │   ├── ADR-0001-tenant-equals-stack.md
│   │   └── ADR-0002-iam-first.md
│   │
│   ├── 03-runbooks/        # Betrieb & Nutzung (später)
│   │   └── README.md
│   │
│   └── 04-threat-model/    # Risiken & Trust Boundaries (später)
│       └── README.md
│
├── infra/                  # Infrastruktur & Templates (ab v0.2)
│   ├── edge/
│   │   └── README.md
│   ├── core/
│   │   └── README.md
│   └── tenants/
│       └── tenant-template/
│           └── README.md
│
├── scripts/                # Automatisierung (ab v0.6/v0.7)
│   └── README.md
│
├── secrets/                # NIE committen
│   └── README.md
│
└── .vscode/                # optional, später bewusst
    └── extensions.json