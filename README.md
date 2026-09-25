# Idea Vault — Kumpulan Ide Projek Hackathon Tema RWA

Koleksi 16 ide aktif projek hackathon siap dipilih dan dikembangkan, tema utama **Real World Assets (RWA)** — kombinasi dengan **ZK** atau **AI** hanya dipakai bila esensial untuk mekanisme, bukan tempelan. Lima batch riset: batch pertama (10 kandidat, 5 terpilih, 3 kemudian dieliminasi pengguna), batch kedua September 2026 (5 kandidat, 3 terpilih — fokus likuiditas sekunder & oracle NAV), batch ketiga September 2026 (5 kandidat B2C, semuanya terpilih — platform/tools retail untuk aktivitas on-chain RWA), batch keempat September 2026 (5 kandidat dApps, 3 terpilih — dApps konsumen yang memarkir dana tertahan di token RWA ber-yield dan mengembalikan float ke pemiliknya), dan batch kelima September 2026 (5 kandidat DeFi protocol — perp DEX, margin, vault underwriting — 3 terpilih). Dipilih berdasarkan kriteria penilaian di bawah.

> **Cara pakai:** mulai dari tabel navigasi, baca file ide yang menarik, cek skenario demo day dan tabel kelemahan sebelum memutuskan. Rekomendasi batch pertama: **BoundProof** (#2). Rekomendasi batch kedua: **ClearExit** (B#1). Rekomendasi batch ketiga: **PoolParty** (C#1). Rekomendasi batch keempat: **Pusaka** (D#1). Rekomendasi batch kelima: **MarginYield** (E#1).

---

## Navigasi

| # | File | Projek | Ringkasan | Teknologi | Ranking |
|---|---|---|---|---|---|
| 2 | [02-boundproof.md](02-boundproof.md) | **BoundProof** | Proof-of-backing token treasury/fund dengan input zkTLS terikat sumber + nullifier registry anti double-backing | RWA + ZK | #2 |
| 5 | [05-carryx.md](05-carryx.md) | **CarryX** | Implementasi pertama FRS (token negative-carry): biaya simpan ter-encode on-chain, q(t) decay + adapter ERC-4626 sadar-carry | RWA | #5 |
| 6 | [06-clearexit.md](06-clearexit.md) | **ClearExit** | Rail exit lelang harga seragam (uniform-price batch auction) untuk token RWA redeemable: splitter dapat harga identik, proration on-chain, kurator dihapus | RWA | **B#1** |
| 7 | [07-pulseband.md](07-pulseband.md) | **PulseBand** | Uniswap v4 hook "oracle slip-band" untuk pool RWA: fee meledak saat feed NAV basi, order besar di-revert ke rail redemption, kupon mengalir ke LP | RWA + DeFi hooks | B#2 |
| 8 | [08-navkeep.md](08-navkeep.md) | **NAVKeep** | Tangga kontinuitas pricing saat feed NAV mati: tier FRESH/STALE/DEAD, harga pasar ter-clamp band menyempit, freeze terjadwal — jawaban untuk kematian oracle | RWA + oracle arch | B#3 |
| 9 | [09-poolparty.md](09-poolparty.md) | **PoolParty** | Vault mikro-akses retail: pecah barrier minimum dana RWA ($20 vs $5M per-chain untuk fund yang sama) lewat wrapper subscriber tunggal + micro-share ERC-4626 dengan accrual pro-rata | RWA | **C#1** |
| 10 | [10-agentleash.md](10-agentleash.md) | **AgentLeash** | Policy contract on-chain untuk AI agent portofolio RWA: 7 kontrol session key + cek RWA-aware (eligibility ERC-3643, staleness NAV, konsentrasi issuer), attack replay insiden Bankrbot | RWA + AI + ERC-4337 | C#2 |
| 11 | [11-bayardiri.md](11-bayardiri.md) | **BayarDiri** | Pinjaman retail ber-kolateral token RWA yield-bearing: accrual kolateral otomatis membayar bunga + pokok — utang menyusut per blok sampai self-liquidation | RWA (lending) | C#3 |
| 12 | [12-gatecover.md](12-gatecover.md) | **GateCover** | Proteksi parametrik retail terhadap redemption gate: trigger dibaca dari state on-chain fund (queue depth, TWAP diskon NAV), severity-proportional payout | RWA + parametrik | C#4 |
| 13 | [13-netyield.md](13-netyield.md) | **NetYield** | Vault retail "APY jujur": net APY riil per produk (fee aktual, waiver, carry, biaya exit) + rotasi otomatis sadar-friksi + scorecard publik APY iklan vs nyata | RWA (agregasi) | C#5 |
| 14 | [14-pusaka.md](14-pusaka.md) | **Pusaka** | Warisan akun RWA: fallback inaktivitas bertingkat (warning → grace → klaim) di akun ERC-4337 + pre-registration ahli waris di identity registry agar transfer token permissioned tidak revert | RWA + ERC-4337 | **D#1** |
| 15 | [15-arisyield.md](15-arisyield.md) | **ArisYield** | Arisan on-chain dengan pot idle diparkir token T-bill ber-yield: yield terbagi pro-rata berbobot waktu tunggu (rotasi akhir dapat bagian terbesar), undian VRF, kontrak menggantikan bendahara | RWA | D#2 |
| 16 | [16-jatuhtempo.md](16-jatuhtempo.md) | **JatuhTempo** | Penjadwal liabilitas & target ber-yield: tanggal jatuh tempo jadi input utama, sweep otomatis USDC idle ke token RWA instant-redeem, auto-redeem H-1, auto-bayar di tanggal H | RWA + otomasi on-chain | D#3 |
| 17 | [17-marginyield.md](17-marginyield.md) | **MarginYield** | Token margin T-bill untuk perp DEX: margin = share vault instant-redeem ber-accrual per-detik, loss/fee diselesaikan auto-redeem hanya slice terpakai, floor RWA 4–5% ungated | RWA + perp margin | **E#1** |
| 18 | [18-diviperp.md](18-diviperp.md) | **DiviPerp** | Perp ekuitas sadar-dividen & aksi korporat: funding atas indeks total-return, dividend accrual ledger on-chain, adjustment engine atomik saat split/merger (replay insiden Ventuals SPCX) | RWA + perp engine | E#2 |
| 19 | [19-rateperp.md](19-rateperp.md) | **RatePerp** | Perpetual pada level yield tokenized treasury: kontrak "APY points", index dari accrual rate on-chain + implied rate Pendle TWAP, oracle tak pernah tidur — hedge Fed cut & FOMC 24/7 | RWA + rate derivatif | E#3 |

> Ranking `#1–#5` = batch pertama, `B#1–B#3` = batch kedua (riset September 2026), `C#1–C#5` = batch ketiga B2C (riset September 2026), `D#1–D#3` = batch keempat dApps (riset September 2026), `E#1–E#3` = batch kelima DeFi protocol (riset September 2026); antar-batch tidak digabung-ranking.

---

## Asal-Usul Ide

Ide-ide di koleksi ini **tidak dibuat dari nol**. Semua diangkat dari riset sumber eksternal, lalu diberi pembeda fitur. Sumber riset (September 2026, jendela 6 bulan ke belakang):

### Proyek hackathon
- **ETHGlobal** (HackMoney 2026, Cannes, New York 2026, New Delhi): RWAlink, Veris, AssetX, AssetLink, REStandard, Orbit, RACE, Mand(ate), ACN, SmartRenovate
- **Chainlink Convergence 2026**: SentinelFi (covenant monitoring via CRE median consensus)
- **Mantle / Casper 2026**: zk-rwa-kit (session credential TLSNotary), PROVENANCE (staked AI rating + rubrik deterministik), ARIA (dewan agen underwriting)

### Paper ilmiah
- **RWA-PoB** (arXiv 2608.25269) — credential-based proof-of-backing, BCR/RLC + repo `rischanlab/PoB`
- **FRS** (arXiv 2606.26704, Matrixdock) — fungible reserve standard, carrying cost on-chain
- **LPOR** (arXiv 2606.08211) — layered proof of reserves, ledger liabilitas user-verifiable
- **SoK RWA** (arXiv 2604.06608), **Taksonomi RWA** (arXiv 2606.08534) — arsitektur, gap dokumentasi
- **RQP** (ePrint 2026/1330) — real-world qualification proof, kredensial terikat issuer + zkSNARK

### Data onchain & pasar
- **rwa.xyz** — tokenized credit $6,99–7,48 miliar distributed (Jul–Agu 2026)
- **Fitch / Proskauer / KBRA** (Sep 2026) — kanyon default rate 1–2% vs 6,3% vs 2,51%
- **BSP Filipina** (Feb 2026) — remitansi OFW rekor $35,63 miliar
- **Kemenkop Indonesia** (Jan & Nov 2025) — 8 koperasi gagal bayar Rp 26 triliun
- **CIFOR-ICRAF** (2025) — 2 juta KK petani sawit rakyat, gap pembiayaan
- **UNESCAP / OECD** — ASEAN Single Window, e-Form D >1 juta dokumen/tahun

### Stack industri (acuan mekanisme)
zkMe/zkOBS, zkPass (nullifier registry), DIA ZK (threshold proof), RedStone Settle, Securitize/RedStone Trusted Single Source Oracle, Maple/Centrifuge (via DeepWiki).

### Riset Batch 2 (September 2026) — sumber ide 06–08

Fokus riset: likuiditas sekunder & exit RWA, keandalan oracle NAV, akuntabilitas underwriter, rekonsiliasi dokumen pra-tokenisasi. Via exa + DeepWiki (Uniswap v4-core, Centrifuge, Maple).

- **Paper**: Prop RFQ (ePrint 2026/1739 — exit pricing pressure-aware, mengakui gap order-splitting), Tang (arXiv 2609.15797 — information recovery via trading, teori RWA), Wharton WIFPR (Mei 2026 — speed matching principle)
- **Produk live**: Symbiotic instant liquidity vault, KPK USDC RWA vault (kurator menetapkan diskon), Upshift RWA Clear (oracle + spread), Uniswap continuous-clearing-auction (uniform price, sisi issuance)
- **Analisis industri**: Stobox liquidity gap ($33,5B on-chain, >50% idle, kasus BCRED gate $3,7B), Gate Learn/TechFlow (resep slip-band + hooks + yield bridging untuk AMM RWA, post-mortem Nest nALPHA/nBASIS), Tokenomics.net (tiga eksposur oracle RWA, "thirty-day blind window"), RWA Bible (gates & proration baru di dokumen legal)
- **Hackathon 2026 baru**: CloakSwap RWA (hook privasi eligibility), Index-Fi (basket vault mock oracle), Sugarc/Kyro/FlowFi/Kora/InvoFlow (faktur — padat, AI risk-scoring), Parametrix/Arc Climate Pay/Reflex (asuransi parametrik cuaca — padat)
- **Enterprise**: POSCO×LG CNS×Injective (receivables + AI review LC), POSCO America×Olea×Intain (rekonsiliasi dokumen pra-onchain), NetNet RWA Desk (premium floor guard issuance)

### Riset Batch 3 (September 2026) — sumber ide 09–13

Fokus riset B2C: platform/tools retail untuk aktivitas on-chain RWA (akses, lending, proteksi, agregasi, agent). Via exa + DeepWiki.

- **Dokumen legal & data akses**: prospektus FOBXX/BENJI minimum per-chain ($20 Stellar s.d. $5.000.000 Ethereum, Juli 2025), Form D BUIDL amandemen Juli 2026 (minimum $100k, redemption $250k), halaman OUSG ($5k instan/$100k non-instan, accredited-only), limit redemption instan OUSG $50M/24 jam — via web3aiblog + eco.com (September 2026)
- **Insiden & riset keamanan agent**: Bankrbot/Grok 4 Mei 2026 (prompt injection morse, 3B DRB $150–200k, tx hash publik, guardrail dihapus pre-launch), CoinDesk April 2026 (26 router MCP injeksi, satu drain $500k), riset a16z 28 April 2026 (agent reproduksi eksploit + lolos sandbox), PromptMink (supply chain npm agent), Freysa (preseden), MetaMask Agent Wallet Guard/Beast Mode + Ledger DMK + Coinbase CDP/Alchemy session keys (guardrail vendor generik, September 2026)
- **Produk & event likuiditas**: BCRED gate $3,7M/$82M (Stobox), RWA Bible gates/proration (Agustus 2026), KPK/Symbiotic/Upshift (ekonomi diskon exit), Alchemix (preseden self-repaying loan 2021 — di luar jendela 6 bulan, kombinasi RWA-nya yang baru)
- **Fees & transparansi**: FRS (fee tersembunyi level issuer), waiver OUSG dengan tanggal tidak konsisten antar sumber, expense BENJI 0,22%, diskon exit KPK 0,05–3%
- **Kompetitor hackathon B2C**: RWAGpt + Orbit (agent RWA tanpa policy layer), Index-Fi (basket mock oracle), PawnStars (lending RWA self-minted, AI pricing), Parametrix/Arc Climate Pay/Reflex/Paramify/Paramora (parametrik — semua trigger eksternal fisik)

### Riset Batch 4 (September 2026) — sumber ide 14–16

Fokus riset dApps: aplikasi konsumen yang memarkir dana tertahan di token RWA ber-yield dan mengembalikan float ke pemiliknya. Via exa + DeepWiki (eth-infinitism/account-abstraction).

- **Data Indonesia**: BPS 2025 (16,18% penduduk usia 10+ ikut arisan, DIY 58,82% — via periskop.id/GoodStats Jun 2026), IJEIRC (Mar 2025 — 249 putusan pengadilan arisan online 2018–2024, puncak 2021), OJK (Mei 2025 — peringatan arisan online ponzi), jurnal pidana Surakarta (Mar 2026 — Pasal 486/492 KUHP)
- **Gelombang ROSCA-onchain 2025–26**: Roda (Arc — escrow + dynamic collateral withholding), CROSCA (DoraHacks — klaim pasar ROSCA global $100B+/tahun), Crosca (Initia), Moigye (VeryChain), LedgerLoop (GNN) — semua pot USDC polos tanpa yield; Observers (Agu 2025) post-mortem gelombang 2016–2022 (Bloinx, Daret, Njangi, Nexspecto)
- **Pembayaran freelance**: Jobbers 2026 (n=22.847, 62 negara — rata-rata 39 hari invoice-to-cash, platform-mediated 37 hari vs direct 12 hari), Upwork Escrow Instructions (dispute window wajib, "sole discretion" menahan dana), UK Small Business Commissioner 2025 (£26 miliar outstanding, 86 jam/tahun kejar tagihan), Trolley 2026 (93% rela discount demi payout 24 jam); escrow web3: GigRevo (auto-release 7 hari), SolSafeHold, web3escrow, DealBlock, TrustLedger, SmarTrust
- **Treasury RWA**: Stable Sea×WisdomTree (Agu 2026 — >$5T kas bisnis AS idle, RWA $6B→$31B), ZKsync Prividium (25–40 bps hilang oleh operasi manual), Liquid Treasury $TSY (accrual per-detik + redemption instan 24/7, API-first), ACT Tomorrow's Treasury (Jan 2026), McKinsey via tempo.xyz (nostro 34%)
- **Warisan crypto**: Chainalysis (2,3–3,7 juta BTC hilang permanen, 11–18% suplai), BofA 2024 ($6 triliun via warisan sampai 2045), Ledger Academy (Des 2025), Startup Fortune (Apr 2026), CryptoSens (Feb 2026), Tangem (Apr 2026); produk Liana/Nunchuk/Sarcophagus/Evoke/Casa/Unchained; DeepWiki ERC-4337 (validAfter/validUntil = building block, logika inactivity-recovery harus custom)
- **Deposit sewa**: TDS Statistical Briefing 2024/25 (4,7 juta deposit senilai £5,53 miliar di Inggris & Wales), mydeposits (Agu 2025 — landlord menang klaim penuh <20% kasus), property118 (estimasi float skema ±£230 juta/tahun, label estimasi)

### Riset Batch 5 (September 2026) — sumber ide 17–19

Fokus riset DeFi protocol: perp DEX RWA, margin trading, yield trading, vault underwriting. Via exa + DeepWiki (pendle-finance/pendle-core-v2-public). Area yang terverifikasi PADAT dan sengaja dihindari: fixed-yield treasury (Pendle dominan — $69,8B settled, market PT-thBILL/eACRED/USDG/apyUSD), lending kolateral RWA institusional (Aave Horizon $600M deposit, VBILL LTV 88%, weakness NAV-staleness terdokumentasi Mirador Jan 2026), RWA perp polos (TradeXYZ/Ostium/GMTrade/Lighter), covered call manual (xOptions Devpost).

- **Laporan pasar perp**: Alea RWA Perpetuals (Jul 2026 — OI $4,3B 15x YTD; TradeXYZ 56,9%; 65% volume RWA perp di luar jam AS), CoinMarketCap State of the Market (Mei 2026 — ekuitas 5%→28% volume mingguan 4 bulan, $2,7B→$15,6B/minggu; kutipan "dividends ignored → structural premia"; bucket Bonds "single-venue, negligible"; proyeksi $60–80B/minggu Q4 2026), DWF Labs 2 laporan (Mar + Jul 2026 — insiden Ventuals SPCX: crash 45%/30 menit, 405 likuidasi, $1,51M, data provider salah olah split 5:1; risiko sentralisasi oracle; HIP-3: stake 500k HYPE, deployer 50% fee; GMTrade vault per-market 22,6% volume; CFTC framework + Kalshi BTCPERP), Blockscholes (Mar 2026 — Hyperliquid $2B→$8B/hari 2025, proyeksi $32B/hari 2026)
- **Dokumen venue**: Hyperliquid portfolio margin docs + unified account guide (default USDC-only 0 yield; PM gated $10k/$5M, cap $25M, rate utilization-based, USDC supply cap $1B; kutipan undangan build EVM yield-bearing ERC20), Ostium docs (USDC segregated tanpa yield, $46B kumulatif, 95%+ OI non-kripto)
- **Yield infra**: Pendle docs + Pendle Print #105 + AiCoin + CoinGecko Apyx (PT-thBILL 5,35%; YT-apyUSD leverage efektif 59x; Apyx $237M TVL; Boros = funding rate swap kripto; IRS TradFi $400T+), DeepWiki pendle-core-v2 (getMarketLnImpliedRate TWAP, PendleChainlinkOracle, SY ERC4626_NOT_REDEEMABLE), Liquid Treasury $TSY (accrual per-detik + redemption instan 24/7)
- **Ekuitas ter-tokenisasi**: xStocks live di Hyperliquid Agu 2026 (NVDAx/SPYx/QQQx/SKHYx/MUx + wrapper ERC-4626 di HyperEVM; v1 wrapper donation-bug), xChange RFQ engine (Mar 2026)

## Konteks Seleksi Batch 5 (DeFi protocol)

Dari riset DeFi September 2026 lahir 5 kandidat; 3 masuk (17–19), 2 gugur. Kriteria seleksi (diminta pemilik repo): problem yang dicoba diselesaikan, kemenarikan tech untuk hackathon, potensi bisnis pasca-hackathon — **dinilai berbasis data, terutama sisi bisnis**.

| Kandidat | Status | Alasan |
|---|---|---|
| **EquityCarry** (vault delta-neutral "internet bond" ekuitas: pegang xStock + short perp sama notional, panen funding + dividen) | Gugur | Kasus bisnis bertumpu funding rate perp ekuitas persisten positif — **tidak ada satu pun sumber riset yang menguantifikasinya**; pola Ethena terbukti rentan episode funding negatif; kompetitor head-start langsung Apyx (yield dividen DAT, $237M TVL dalam hitungan bulan) dengan jalur lebih sederhana tanpa hedge keeper; kategorinya optimasi yield, bukan problem |
| **FeedGuard** (vault underwriting lintas market dengan exposure cap ditentukan skor kesehatan feed on-chain deterministik) | Gugur | Mekanisme paling elegan di batch, tapi bisnis terlemah: kerugian Ventuals $1,51M menimpa trader via likuidasi, bukan LP — tesis underwriter-menanggung-ekor tidak langsung; model LP vault perp masih ceruk (GMTrade 22,6% volume, "slowly growing"); return underwriting tak terkuantifikasi sumber mana pun; adjacency ke PulseBand (07) = proteksi LP via fee spike vs via exposure cap |

Pemenang batch: **MarginYield** (E#1 — waste terukur langsung: margin 0% vs floor 4,5% + kutipan undangan resmi Hyperliquid + matematika revenue $4,5–9 juta/tahun per $1 miliar adopsi + preseden vault 8,9% APY), **DiviPerp** (E#2 — data insiden paling keras $1,51M + kategori tumbuh 5,7x/kuartal + demo split replay terbaik; posisi bisnis = lisensi engine ke deployer HIP-3, bukan perang venue; risiko regulasi single-name paling nyata — jujur dicatat), **RatePerp** (E#3 — bucket kosong terkonfirmasi + $31B underlying tumbuh 5x/18 bulan + oracle dari state on-chain sendiri + kemitraan issuer instant-redeem paling masuk akal; demand belum terbukti = alasan utama posisi tiga).

Catatan overlap yang dijaga tegas: RatePerp vs Pendle = instrumen directional tanpa maturity vs pasar fixed-yield (komplementer — PT holder jadi pengguna hedging alami); MarginYield vs BayarDiri (11) = margin trading vs pinjaman retail; MarginYield & JatuhTempo (16) berbagi primitif instant-redeem untuk keperluan berbeda (settlement vs kepastian tanggal); DiviPerp berdiri sendiri sebagai satu-satunya ide derivatif ekuitas.


---

## Kriteria Penilaian Ide

### Lapis 1 — 4 pertanyaan juri hackathon

Tiap ide harus bisa menjawab **dengan data**:

1. **How effectively does the project address a genuine real-world problem or use case?** — masalah nyata, bukan masalah buatan; ada angka keras pendukung
2. **How meaningfully does the project use Ethereum, smart contracts, tokenization, or other onchain infrastructure?** — logika inti hidup di kontrak, bukan dashboard pelaporan pasif
3. **How novel is the solution compared to existing approaches to RWA?** — kebaruan level fitur/mekanisme terhadap proyek dan paper yang sudah ada
4. **Can the solution realistically be deployed, adopted, and scaled beyond the hackathon?** — jalur adopsi pasca-hackathon bisa diceritakan kredibel

### Lapis 2 — kriteria internal koleksi ini

- **Diferensiasi di level fitur/mekanisme**, bukan regulasi atau hal yang tidak terlihat di demo
- **Grounding riset**: ide diangkat dari paper/proyek/data nyata, tidak dikarang dari nol
- **Demo-able**: fungsionalitas dan inovasi bisa disaksikan hidup-hidup di demo day (tx revert, angka berubah, transaksi nyata)
- **Kombinasi ZK/AI tidak dipaksakan** — hanya bila esensial untuk mekanisme
- **Kejujuran kelemahan**: tiap file punya tabel kelemahan + mitigasi; tidak ada confidence dipaksakan
- **Kelemahan bisa dimaklumi atau bisa diakali** — ini kriteria utama seleksi top 5
- **Kelayakan bisnis** — pasar dan model usaha masuk akal

---

## Aturan & Konvensi Direktori

### Struktur wajib tiap file ide

```
1. Judul + elevator pitch (1 paragraf)
2. Latar belakang & data pasar (angka keras + sumber)
3. Tabel grounding riset (paper / proyek / data, dengan link)
4. Problem statement
5. Pembeda fitur (numbered, level mekanisme)
6. Jawaban 4 pertanyaan juri (dengan data)
7. Teknologi (RWA + ZK/AI + stack demo)
8. High-level e2e flow — WAJIB diagram mermaid, bukan prosa
9. Skenario demo day (urutan aksi yang terlihat)
10. Tabel kelemahan & mitigasi
11. Roadmap pasca-hackathon
```

### Konvensi

- **Penomoran**: file ide bernomor urut `01-`, `02-`, ... sesuai ranking. `README.md` (file ini) adalah index.
- **Menambah ide baru**: salin struktur wajib di atas, nomor berikutnya, update tabel navigasi di file ini, catat di bagian "gugur/aktif".
- **Membuang ide**: saat ada perintah eksplisit dari pemilik repo untuk membuang/eliminasi sebuah ide, **pindahkan** file `.md` ide tersebut ke folder `bucket/` — jangan dihapus. Kalau folder `bucket/` belum ada, buat dulu foldernya sebelum memindahkan. Setelah memindahkan: hapus baris ide dari tabel navigasi di file ini, dan catat pembuangan tersebut di bagian "Ide Tereliminasi oleh Pengguna" (nama ide + tanggal + file sekarang ada di `bucket/`). Nomor file lain tidak digeser.
- **Diagram mermaid** hanya ter-render di viewer yang mendukung: VS Code preview, GitHub, Obsidian. Di editor plain text terlihat sebagai blok kode.
- **Bahasa**: Indonesia untuk semua file; istilah teknis tetap bahasa Inggris (NAV, zkTLS, circuit breaker, dll).
- **Jangan hapus bagian kelemahan** saat mengedit — itu bagian dari kriteria kejujuran koleksi.

---

## Konteks Seleksi: 5 Ide yang Gugur

Dari 10 ide hasil riset (5 global + 5 ASEAN), lima berikut tidak masuk karena kelemahannya tidak memenuhi kriteria "bisa dimaklumi/diakali":

| Ide | Alasan gugur (satu baris) |
|---|---|
| TrueMark (NAV band independen) | Sumber valuasi independen utk kredit privat nyaris tak ada di produksi — kelemahan kena inti nilai; demo berisiko jadi konsensus mock |
| ExitLane (lelang likuidasi patuh) | Premis intinya bertumpu regulasi (compliance blocks liquidators) — bertentangan dengan kriteria pembeda level fitur |
| SijilPay (escrow e-Form D ASEAN) | Produksi butuh akses portal Single Window pemerintah — dependensi struktural di luar jangkauan tim hackathon |
| WaqfFlow (CWLS ter-tokenisasi) | Produksi butuh restu Kemenkeu/BWI; data emisi CWLS terlemah dari semua ide |
| TandanToken (replanting sawit) | Demo melibatkan banyak aktor + float 3–4 tahun; paling sulit dipadatkan jadi demo meyakinkan |

Ide-ide ini tetap punya nilai — bisa dihidupkan ulang bila konteks berubah (mis. kemitraan pemerintah tersedia, atau hackathon dengan durasi lebih panjang).

## Ide Tereliminasi oleh Pengguna

| Ide | Alasan |
|---|---|
| KopraGuard (01) | Dienalinasi pengguna, September 2026 — tidak akan dipakai; file dihapus |
| PadalaProof (04) | Dienalinasi pengguna, September 2026 — tidak akan dipakai; file dihapus |
| DefaultLens (03) | Dienalinasi pengguna, 25 September 2026 — tidak akan dipakai; file sekarang ada di `bucket/` |

Penomoran file tidak digeser setelah penghapusan (konvensi `01-`, `02-`, ... tetap menunjukkan urutan asli batch pertama).

> **Prosedur berlaku mulai sekarang:** pembuangan ide tidak lagi berarti penghapusan file. File `.md` ide yang dibuang dipindahkan ke folder `bucket/` (folder dibuat dulu bila belum ada) — lihat konvensi "Membuang ide" di atas. KopraGuard dan PadalaProof terhapus permanen sebelum konvensi ini dibuat, jadi tidak ada di `bucket/`.

## Konteks Seleksi Batch 2

Dari riset September 2026 lahir 5 kandidat; 3 masuk (06–08), 2 ditunda, 2 gugur saat verifikasi kebaruan:

| Kandidat | Status | Alasan |
|---|---|---|
| **SkinPool** (fee-at-risk escrow underwriter + track record on-chain, grounding DeepWiki Maple) | Ditunda | Mekanisme solid tapi inkremental terhadap StakeLocker Maple; track record registry berbau analitik — dilemahkan untuk demo. Bisa dihidupkan bila butuh sudut kredit privat |
| **MatchGate** (gate rekonsiliasi lintas dokumen pra-mint dengan AI ekstraksi + rules deterministik, grounding pilot POSCO×Intain) | Ditunda | Grounding enterprise kuat, tapi ruang faktur 2026 sudah padat (Sugarc, Kyro, FlowFi, Kora, InvoFlow) dan mekanisme challenge attester kompleks untuk hackathon |
| Asuransi parametrik cuaca untuk RWA | Gugur | Terlambat: Parametrix (2 versi), Arc Climate Pay, Reflex, Paramify, Paramora sudah memenuhi niche 2025–2026 |
| Premium-gated issuance untuk DAT | Gugur | NetNet RWA Desk sudah implementasi (floor guard 1,2× backing, discount cap immutable, ratchet) — kebaruan hilang |

## Konteks Seleksi Batch 3 (B2C)

Dari riset B2C September 2026 lahir 7 kandidat; 5 masuk (09–13), 2 gugur saat penyaringan:

| Kandidat | Status | Alasan |
|---|---|---|
| **GatePulse** (prediction market pada event gate fund) | Gugur | Satu tema gates hanya kuat untuk satu produk — GateCover dipilih karena value prop retail lebih langsung (kompensasi vs spekulasi) dan tidak bawa optics gambling; sinyal pasar ala GatePulse bisa jadi fitur lanjutan GateCover (policy sekunder) |
| **ExitScore** (dashboard exit-ability retail ala "3 pertanyaan Stobox") | Gugur | Analitik berat, mekanisme tipis — lemah di pertanyaan juri #2 (logika inti tidak hidup di kontrak); metriknya diserap sebagai komponen NetYield & GateCover |

Catatan overlap yang disengaja dijaga tegas: NetYield vs CarryX (05) = produk agregasi retail vs standard/adapter satu token; GateCover vs ClearExit (06) = kompensasi holder saat rail macet vs rail exit itu sendiri — komplementer.

## Konteks Seleksi Batch 4 (dApps)

Dari riset dApps September 2026 lahir 5 kandidat; 3 masuk (14–16), 2 ditunda. Kriteria seleksi batch ini: problem yang disolve, kemenarikan di hackathon, potensi bisnis pasca-hackathon.

| Kandidat | Status | Alasan |
|---|---|---|
| **YieldEscrow** (escrow milestone freelance ber-yield: dana parkir token T-bill selama hold, bunga ke penerima akhir, diam = bayar) | Ditunda | Kebaruan paling tipis dari lima: auto-release sudah ada (GigRevo), ruang escrow web3 ramai 6+ produk, yield pada hold 39 hari ±0,4% — nominal kecil; satu keluarga mekanisme dengan JaminFlow (ditunda juga), bisa dihidupkan sebagai vertikal kerja bila konteks berubah |
| **JaminFlow** (deposit sewa + prepaid rent ber-yield: bunga milik penyewa, diam = kembali, landlord klaim ber-stake) | Ditunda | Data keras (£5,53 miliar deposit TDS) tapi cold start dua sisi yang cacat struktural: landlord — pihak pengendali deal — kehilangan float bila ikut, tanpa insentif; lebih kuat sebagai modul produk properti daripada produk berdiri sendiri |

Pemenang batch: **Pusaka** (D#1 — kebaruan terkonfirmasi gap ERC-4337 + masalah irreversible + model bisnis willingness-to-pay terbukti), **ArisYield** (D#2 — data lokal terkeras + demo paling teatrikal), **JatuhTempo** (D#3 — jawaban terkuat "logika inti di kontrak" + jalur B2B jelas).

Catatan overlap yang dijaga tegas: JatuhTempo vs NetYield (13) = engine kepastian tanggal vs produk optimasi APY — komplementer; Pusaka memakai ERC-4337 seperti AgentLeash (10) tapi domainnya berbeda jauh (suksesi aset vs policy agent).

---

## Tanggal Riset & Disclaimer

- **Riset: September 2026** (jendela 6 bulan ke belakang; batch kedua, ketiga, keempat, dan kelima via exa + DeepWiki), via pencarian web + exa + deepwiki.
- Semua angka pasar (rwa.xyz, Fitch, BSP, Kemenkop, CIFOR, UNESCAP, minimum per-chain BENJI, Form D BUIDL, APY/waiver OUSG) adalah pembacaan saat riset — **bisa basi**. Verifikasi ulang angka kunci sebelum dipakai di pitch/README hackathon.
- Referensi proyek hackathon adalah karya pihak lain — ide di koleksi ini membangun di atasnya dengan pembeda fitur, bukan menyalin. Sebutkan referensi di kredit saat presentasi.
