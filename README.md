# Idea Vault — Kumpulan Ide Projek Hackathon Tema RWA

Koleksi 5 ide projek hackathon siap dipilih dan dikembangkan, tema utama **Real World Assets (RWA)** — kombinasi dengan **ZK** atau **AI** hanya dipakai bila esensial untuk mekanisme, bukan tempelan. Hasil kurasi dari **10 ide** hasil riset September 2026 (5 sudut global + 5 sudut ASEAN), dipilih berdasarkan kriteria penilaian di bawah.

> **Cara pakai:** mulai dari tabel navigasi, baca file ide yang menarik, cek skenario demo day dan tabel kelemahan sebelum memutuskan. Rekomendasi utama: **KopraGuard** (peringkat #1).

---

## Navigasi

| # | File | Projek | Ringkasan | Teknologi | Ranking |
|---|---|---|---|---|---|
| 1 | [01-kopraguard.md](01-kopraguard.md) | **KopraGuard** | Proof-of-backing simpanan koperasi: ledger liabilitas terverifikasi anggota + circuit breaker on-chain mencegah Ponzi tumbuh | RWA + ZK | **#1** |
| 2 | [02-boundproof.md](02-boundproof.md) | **BoundProof** | Proof-of-backing token treasury/fund dengan input zkTLS terikat sumber + nullifier registry anti double-backing | RWA + ZK | #2 |
| 3 | [03-defaultlens.md](03-defaultlens.md) | **DefaultLens** | Registry kejadian kredit machine-readable dengan definisi parametrik (Fitch-style vs manager-style) + hook waterfall kontrak | RWA + AI | #3 |
| 4 | [04-padalaproof.md](04-padalaproof.md) | **PadalaProof** | Kredensial kredit dari streak remitansi OFW via zkTLS; cicilan auto-split dari remitansi masuk | RWA + ZK | #4 |
| 5 | [05-carryx.md](05-carryx.md) | **CarryX** | Implementasi pertama FRS (token negative-carry): biaya simpan ter-encode on-chain, q(t) decay + adapter ERC-4626 sadar-carry | RWA | #5 |

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

---

## Tanggal Riset & Disclaimer

- **Riset: September 2026** (jendela 6 bulan ke belakang), via pencarian web + exa + deepwiki.
- Semua angka pasar (rwa.xyz, Fitch, BSP, Kemenkop, CIFOR, UNESCAP) adalah pembacaan saat riset — **bisa basi**. Verifikasi ulang angka kunci sebelum dipakai di pitch/README hackathon.
- Referensi proyek hackathon adalah karya pihak lain — ide di koleksi ini membangun di atasnya dengan pembeda fitur, bukan menyalin. Sebutkan referensi di kredit saat presentasi.
