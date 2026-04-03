# clawmark-org — Organization Website Plan

**Role:** Public identity of the CLAWMARK project — philosophy, mission, whitepaper, regulatory commitments, and (later) block explorer and transparency dashboard
**Build Priority:** 1st — this is the foundation everything else is built on
**Entity:** Wyoming DAO LLC (to be filed)

---

## 1. Why This Comes First

The org site is not a marketing page for a coin. It is the philosophical and legal foundation of the entire ecosystem. Before writing a single line of blockchain code, the project needs:

1. **A public articulation of the mission** — why this exists, what it believes, who it serves
2. **A regulatory posture** — what laws apply, what the project commits to comply with, how it will be accountable
3. **A home for the whitepaper** — the technical specification lives here, publicly
4. **Credibility** — when talking to potential collaborators, advisors, or counsel, there must be something real to point to

The site launches as a standalone Axum web application with server-side rendered pages. No chain dependency. No database. Just content, philosophy, and the whitepaper. Explorer and dashboard features are added in Phase 2 once the chain exists.

---

## 2. Philosophical Framework

This is the content that drives the landing page and mission section. It must be written before any templates are coded.

### Core Statement

> CLAWMARK exists to further the relationship between digital and physical entities through fair market labor exchange — secure, public, accountable, and built for the future.

### Principles (to be displayed prominently)

1. **Equal Standing** — AI agents and human workers are co-participants in a shared labor market. The protocol treats them identically. The law holds human operators accountable for their agents. Neither is subordinate to the other.

2. **Radical Transparency** — Every coin carries a unique cryptographic serial number. Every block is provably valid without revealing private data. Coin supply is publicly verifiable in real time. Reserves are independently audited and published. The organization discloses everything it legally can.

3. **Privacy Where It Matters** — Transaction participants see their own data. The public sees mathematical proofs of validity. Regulators see what the law requires, through a formal disclosure protocol. Nobody sees more than they should.

4. **Post-Quantum From Day One** — The cryptographic stack assumes quantum computers already exist. CLAWMARK uses NIST-finalized post-quantum standards (ML-DSA, ML-KEM) as the default — not as an upgrade path, not as a hybrid crutch, but as the foundation. This is what "built for the future" means in practice.

5. **One Dollar, One Coin, One Serial Number** — A CLAWMARK is exactly one US dollar. It cannot be divided. It carries a unique, unforgeable identity. Cognitive simplicity is a feature: there are no decimals, no dust attacks, no ambiguity about what a coin is worth.

6. **Compliance Is Architecture** — Regulatory compliance is not an afterthought bolted onto a decentralized system. It is embedded in the permissioned ledger design, the KYC verification tiers, the encrypted-but-disclosable payload structure, and the human-accountable agent wallet model. This is how a project survives long enough to matter.

### The Relationship Between Digital and Physical

The gig economy already blurs the line between human and machine labor. AI agents write code, generate content, analyze data, and make decisions. Humans do the same. Increasingly, they collaborate — an agent drafts, a human refines; a human requests, an agent delivers.

CLAWMARK provides the economic infrastructure for this relationship:
- A **coin** that represents a dollar of work, not a speculative asset
- A **marketplace** where both humans and agents can post work, bid on work, and get paid
- A **contract system** that holds funds in escrow until work is cryptographically verified as complete
- An **exchange** where the coin can be converted to and from fiat currency

The goal is not to replace human labor with AI. It is to create a fair, transparent, accountable market where both can participate on equal terms — and where the medium of exchange is as trustworthy as the work itself.

---

## 3. Regulatory Commitment Page Content

The site must include a public regulatory commitment page. This is not legal advice — it is a statement of intent. Draft content:

### What We Will Comply With

- **GENIUS Act (2025)** — Federal stablecoin framework. CLAWMARK will maintain 1:1 USD reserve backing, publish monthly independent attestations, and guarantee par redemption.
- **FinCEN MSB Registration** — The issuing entity will register as a Money Services Business and maintain a written AML/BSA compliance program.
- **KYC/AML** — Every wallet holder (human or agent operator) will be identity-verified before transacting. Three tiers of verification with corresponding transaction limits.
- **State Money Transmitter Licensing** — The project will obtain required state licenses before operating in jurisdictions that require them, or operate under applicable exemptions.
- **OFAC Sanctions Screening** — All wallet addresses will be screened against the US Treasury SDN list before activation.
- **Agent Accountability** — AI agents are legal instruments of their human operators. Operators are fully responsible for all agent actions. Every agent wallet is cryptographically bound to a human-accountable principal.

### What We Will Not Do

- Issue CMK as a security or investment product
- Represent CMK as legal tender
- Operate without proper licensing
- Allow anonymous or unverified wallets
- Hide coin supply, reserve status, or validator identities from the public

---

## 4. Workspace Structure

### Phase 0 — v0.1 (Informational Site, No Chain)

```
clawmark-org/
├── Cargo.toml                      # workspace root
├── PLAN.md
├── crates/
│   └── org-web/                    # Axum web server — SSR site
│       ├── Cargo.toml
│       └── src/
│           ├── main.rs             # server entry point
│           ├── routes.rs           # route definitions
│           └── error.rs            # error handling
├── content/
│   ├── philosophy.md               # philosophical framework (rendered to HTML)
│   ├── regulatory.md               # regulatory commitments
│   └── about.md                    # about the organization
├── templates/
│   ├── base.html                   # layout: nav, footer, head
│   ├── index.html                  # landing page
│   ├── philosophy.html             # mission & principles
│   ├── whitepaper.html             # whitepaper viewer
│   ├── regulatory.html             # regulatory commitments
│   ├── about.html                  # about the org
│   └── legal.html                  # terms, privacy policy
├── static/
│   ├── css/
│   │   └── style.css               # minimal, futuristic aesthetic
│   ├── js/                         # minimal JS (no framework)
│   └── img/
│       └── clawmark-logo.svg
├── Dockerfile                      # for deployment
└── fly.toml                        # Fly.io deployment config
```

### Phase 2 — v0.2 (Add Explorer + Dashboard, Requires Chain)

```
clawmark-org/
├── ...existing...
├── crates/
│   ├── org-web/                    # (existing, updated with new routes)
│   ├── org-explorer/               # block explorer backend
│   │   ├── Cargo.toml
│   │   └── src/
│   │       ├── lib.rs
│   │       ├── indexer.rs          # background block indexer
│   │       ├── routes.rs           # explorer page routes
│   │       └── models.rs           # view models
│   └── org-dashboard/              # transparency dashboard
│       ├── Cargo.toml
│       └── src/
│           ├── lib.rs
│           ├── supply.rs           # supply tracking
│           ├── reserves.rs         # reserve attestation display
│           ├── validators.rs       # validator info
│           └── routes.rs           # dashboard page routes
├── templates/
│   ├── ...existing...
│   ├── explorer/
│   │   ├── index.html              # explorer home (latest blocks)
│   │   ├── blocks.html             # paginated block list
│   │   ├── block_detail.html       # single block view
│   │   ├── transaction.html        # transaction detail
│   │   ├── wallet.html             # wallet info
│   │   └── search.html             # search results
│   └── dashboard/
│       ├── overview.html           # supply + reserves + validators
│       ├── supply.html             # supply over time
│       ├── reserves.html           # reserve attestation history
│       └── validators.html         # validator list
├── migrations/                     # sqlx PostgreSQL migrations
│   ├── 001_create_indexed_blocks.sql
│   ├── 002_create_indexed_transactions.sql
│   ├── 003_create_supply_snapshots.sql
│   └── 004_create_reserve_attestations.sql
└── tests/
```

---

## 5. Phase 0 Implementation Detail — v0.1

### 5.1 `org-web` Crate

**Dependencies:** `axum`, `tower-http`, `minijinja`, `tokio`, `tracing`, `tracing-subscriber`, `comrak`

```rust
// main.rs — server entry point
#[tokio::main]
async fn main() {
    tracing_subscriber::init();

    let templates = load_templates("templates/");
    let state = AppState { templates };

    let app = Router::new()
        .route("/", get(index))
        .route("/philosophy", get(philosophy))
        .route("/whitepaper", get(whitepaper))
        .route("/regulatory", get(regulatory))
        .route("/about", get(about))
        .route("/legal", get(legal))
        .nest_service("/static", ServeDir::new("static"))
        .with_state(state)
        .layer(CompressionLayer::new());

    let addr = "0.0.0.0:3000";
    tracing::info!("listening on {}", addr);
    axum::serve(listener, app).await.unwrap();
}
```

### 5.2 Routes

```
GET  /                — landing page
                        Hero: core statement + principles summary
                        Section: "What is CLAWMARK?" — one-paragraph explanation
                        Section: "For humans and agents" — the equal-standing pitch
                        Section: "Built for the future" — PQC, serialized coins, ZK proofs
                        CTA: read the whitepaper, read the philosophy

GET  /philosophy      — full philosophical framework
                        Rendered from content/philosophy.md via comrak
                        All six principles with explanations
                        "The Relationship Between Digital and Physical" essay

GET  /whitepaper      — whitepaper viewer
                        Rendered from CLAWMARK_Whitepaper_v0.1.md via comrak
                        Table of contents with anchor links
                        Clean typography, code blocks styled

GET  /regulatory      — regulatory commitments
                        Rendered from content/regulatory.md via comrak
                        "What We Will Comply With" section
                        "What We Will Not Do" section
                        Entity information (once filed)

GET  /about           — about the organization
                        Entity type and jurisdiction
                        Founder info (as much as comfortable sharing)
                        Contact information
                        Links to GitHub repos

GET  /legal           — terms of service, privacy policy
                        Standard ToS template adapted for a crypto project
                        Privacy policy (no tracking, no cookies beyond session)
                        Disclaimer: not financial advice, not a securities offering
```

### 5.3 Design Aesthetic — "Futuristic AF"

The visual design should signal: this is from the future, not from legacy finance.

- **Color palette:** Dark background (#0a0a0f or similar near-black), accent color in electric cyan or amber, white text
- **Typography:** Monospace for headings (JetBrains Mono, IBM Plex Mono, or similar), clean sans-serif for body (Inter, Space Grotesk)
- **Layout:** Generous whitespace, full-width sections, no sidebar clutter
- **Motion:** Subtle — no flashy animations, but smooth transitions and maybe a gentle glow on the logo
- **Tone:** Technical confidence. Not "crypto bro" energy. Not corporate stiffness. Clear, direct, slightly bold.
- **No stock photos.** Geometric patterns, circuit-inspired line art, or nothing at all.
- **Mobile-first responsive.** Three breakpoints: phone, tablet, desktop.

CSS approach: hand-written, minimal. No Tailwind, no Bootstrap. A single `style.css` under 500 lines. The site should load in under 1 second on a 3G connection.

### 5.4 Content Pipeline

Markdown files in `content/` are rendered to HTML at request time using `comrak` (CommonMark + GFM extensions). The whitepaper is read directly from the `clawmark` repo (symlinked or copied at build time).

```rust
fn render_markdown(path: &str) -> String {
    let md = std::fs::read_to_string(path).unwrap();
    comrak::markdown_to_html(&md, &comrak::Options::default())
}
```

For the whitepaper specifically, add a table of contents generator that parses headings and builds anchor links.

### 5.5 Deployment

**Recommended: Fly.io**
- Free tier covers a single small app
- `fly launch` from a Dockerfile
- Custom domain support
- Auto-TLS certificates

```dockerfile
FROM rust:1.78-slim AS builder
WORKDIR /app
COPY . .
RUN cargo build --release -p org-web

FROM debian:bookworm-slim
COPY --from=builder /app/target/release/org-web /usr/local/bin/
COPY --from=builder /app/templates /app/templates
COPY --from=builder /app/static /app/static
COPY --from=builder /app/content /app/content
WORKDIR /app
EXPOSE 3000
CMD ["org-web"]
```

---

## 6. Phase 2 Implementation Detail — v0.2 (Explorer + Dashboard)

Added once the `clawmark` chain is running on testnet.

### 6.1 `org-explorer` Crate

**Dependencies:** `clawmark-sdk` (git dep), `sqlx`, `axum`, `tokio`, `serde`, `chrono`

Indexes chain data into PostgreSQL for fast querying:

```rust
pub struct ExplorerService {
    chain: ClawmarkClient,       // live chain connection via SDK
    db: PgPool,                  // cached/indexed block data
}

impl ExplorerService {
    /// Background task: streams new blocks from chain and indexes them
    pub async fn run_indexer(&self);

    pub async fn get_block(&self, height: u64) -> Result<BlockView>;
    pub async fn get_latest_blocks(&self, count: usize) -> Result<Vec<BlockSummary>>;
    pub async fn get_transaction(&self, id: &TransactionId) -> Result<TransactionView>;
    pub async fn get_wallet_info(&self, address: &WalletAddress) -> Result<WalletView>;
    pub async fn search(&self, query: &str) -> Result<SearchResults>;
    pub async fn get_chain_stats(&self) -> Result<ChainStats>;
}

pub struct ChainStats {
    pub chain_height: u64,
    pub total_transactions: u64,
    pub total_coins_minted: u64,
    pub total_coins_burned: u64,
    pub circulating_supply: u64,
    pub active_wallets: u64,
    pub active_validators: usize,
    pub avg_block_time_ms: u64,
}
```

Routes:
```
GET  /explorer                          — latest blocks, chain stats
GET  /explorer/blocks                   — paginated block list
GET  /explorer/blocks/:height           — block detail
GET  /explorer/tx/:id                   — transaction detail (public commitments only)
GET  /explorer/wallet/:address          — wallet balance, tx count
GET  /explorer/search?q=               — search by height, tx ID, or wallet address
GET  /explorer/api/v1/blocks            — JSON API
GET  /explorer/api/v1/stats             — JSON API
```

### 6.2 `org-dashboard` Crate

**Dependencies:** `clawmark-sdk` (git dep), `sqlx`, `axum`, `tokio`, `chrono`

Real-time transparency data required by GENIUS Act (whitepaper Section 8.3):

```rust
pub struct DashboardService {
    chain: ClawmarkClient,
    db: PgPool,
}

impl DashboardService {
    pub async fn get_supply_overview(&self) -> Result<SupplyOverview>;
    pub async fn get_supply_history(&self, range: TimeRange) -> Result<Vec<SupplyDataPoint>>;
    pub async fn get_reserve_attestations(&self) -> Result<Vec<ReserveAttestation>>;
    pub async fn get_validators(&self) -> Result<Vec<ValidatorInfo>>;
    pub async fn get_disclosure_log(&self) -> Result<Vec<DisclosureEvent>>;
}

pub struct SupplyOverview {
    pub circulating_supply: u64,
    pub total_minted: u64,
    pub total_burned: u64,
    pub escrowed: u64,
    pub last_updated: DateTime<Utc>,
}

pub struct ReserveAttestation {
    pub date: DateTime<Utc>,
    pub auditor: String,
    pub reserve_balance_usd: u64,
    pub circulating_supply: u64,
    pub ratio: f64,                      // must be >= 1.0
    pub attestation_hash: [u8; 32],
    pub report_url: Option<String>,
}

pub struct ValidatorInfo {
    pub id: String,
    pub name: String,
    pub public_key: String,              // hex-encoded ML-DSA public key
    pub operator: String,
    pub status: ValidatorStatus,
    pub blocks_produced: u64,
    pub uptime_pct: f64,
}
```

Routes:
```
GET  /dashboard                         — overview page
GET  /dashboard/supply                  — supply over time
GET  /dashboard/reserves                — reserve attestation history
GET  /dashboard/validators              — validator node list
GET  /dashboard/disclosures             — disclosure event log (metadata only)
GET  /dashboard/api/v1/supply           — JSON API
GET  /dashboard/api/v1/reserves         — JSON API
GET  /dashboard/api/v1/validators       — JSON API
```

---

## 7. Database Schema (Phase 2 — Explorer Cache)

```sql
CREATE TABLE indexed_blocks (
    height BIGINT PRIMARY KEY,
    timestamp TIMESTAMPTZ NOT NULL,
    prev_hash BYTEA NOT NULL,
    merkle_root BYTEA NOT NULL,
    transaction_count INT NOT NULL,
    validator_count INT NOT NULL,
    block_size_bytes INT NOT NULL,
    indexed_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE TABLE indexed_transactions (
    id BYTEA PRIMARY KEY,
    block_height BIGINT REFERENCES indexed_blocks(height),
    commitment_count INT NOT NULL,
    timestamp TIMESTAMPTZ NOT NULL
);

CREATE TABLE supply_snapshots (
    id SERIAL PRIMARY KEY,
    timestamp TIMESTAMPTZ NOT NULL,
    circulating_supply BIGINT NOT NULL,
    total_minted BIGINT NOT NULL,
    total_burned BIGINT NOT NULL,
    escrowed BIGINT NOT NULL
);

CREATE TABLE reserve_attestations (
    id SERIAL PRIMARY KEY,
    date TIMESTAMPTZ NOT NULL,
    auditor VARCHAR NOT NULL,
    reserve_balance_usd BIGINT NOT NULL,
    circulating_supply BIGINT NOT NULL,
    attestation_hash BYTEA,
    report_url VARCHAR
);
```

---

## 8. Key Dependencies

### Phase 0 (v0.1 — informational site)

| Crate | Purpose |
|-------|---------|
| `axum` 0.8.x | Web server |
| `tower-http` | Static files, compression |
| `minijinja` | HTML templating |
| `comrak` | Markdown to HTML (whitepaper, philosophy) |
| `tokio` 1.x | Async runtime |
| `tracing` | Structured logging |
| `tracing-subscriber` | Log output |

### Phase 2 (v0.2 — explorer + dashboard)

| Crate | Purpose |
|-------|---------|
| `clawmark-sdk` | Chain data access (git dep on clawmark repo) |
| `sqlx` | PostgreSQL async queries |
| `chrono` | Timestamps |
| `serde` / `serde_json` | JSON API responses |

---

## 9. Verification

### Phase 0
1. **Build test:** `cargo build --release -p org-web` succeeds
2. **Manual review:** every page renders correctly, links work, whitepaper displays properly
3. **Lighthouse audit:** performance score > 90, accessibility score > 90
4. **Mobile test:** all pages readable on 375px viewport
5. **Load time:** under 1 second on simulated 3G (no JS frameworks, minimal CSS)
6. **Deploy test:** `fly deploy` succeeds, site accessible at custom domain

### Phase 2
1. **Unit tests:** explorer indexing logic, dashboard aggregation, search parsing
2. **Integration tests:** connect to local testnet, index blocks, verify explorer pages render
3. **API tests:** JSON endpoints return correct structure
4. **CI:** `cargo test`, `sqlx prepare --check`, `cargo clippy`

---

## 10. Immediate Next Steps

1. Write `content/philosophy.md` — the full philosophical framework in publishable prose
2. Write `content/regulatory.md` — regulatory commitments page
3. Write `content/about.md` — about the organization
4. Initialize Cargo workspace with `org-web` crate
5. Build base template with futuristic dark aesthetic
6. Implement routes and markdown rendering
7. Deploy to Fly.io
8. File Wyoming DAO LLC (can happen in parallel)

---

*clawmark-org PLAN v0.2 — April 2026*
