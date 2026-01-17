# Idea to Epic Workflow AI Prompts

Kumpulan prompt AI untuk mengubah ide menjadi Epic & Story yang siap dikembangkan. Bisa digunakan di platform AI manapun (Perplexity, Google Gems, ChatGPT, Claude, dll).

## Gambaran Umum

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  Brainstorming  │────▶│  Product Brief  │────▶│      PRD        │
│     Agent       │     │     Agent       │     │     Agent       │
└─────────────────┘     └─────────────────┘     └─────────────────┘
                                                        │
                        ┌───────────────────────────────┘
                        ▼
┌─────────────────┐     ┌─────────────────┐
│  Architecture   │────▶│ Epics & Stories │────▶  Siap untuk
│     Agent       │     │     Agent       │      Development
└─────────────────┘     └─────────────────┘
```

## Mulai Cepat

1. Pilih platform AI (Perplexity, Google Gems, ChatGPT, Claude)
2. Salin konten file prompt ke custom instructions AI
3. (Opsional) Lampirkan file supporting untuk konteks yang lebih baik
4. Ikuti alur kerja yang dipandu

## Struktur File

```
product-dev-workflow/
├── README.md                    # File ini (Bahasa Indonesia)
├── README.en.md                 # Versi English
├── LICENSE                      # MIT License
├── prompts/
│   ├── 01-brainstorming-agent.md
│   ├── 02-product-brief-agent.md
│   ├── 03-prd-agent.md
│   ├── 04-architecture-agent.md
│   └── 05-epics-stories-agent.md
└── supporting/                  # File referensi opsional
    ├── 01-brainstorming-techniques.md
    ├── 02-product-brief-questions.md
    ├── 03-prd-requirements-framework.md
    ├── 04-architecture-decision-framework.md
    └── 05-epics-stories-guide.md
```

## 5 Agent

| #   | Agent               | Peran               | Fungsi                                        |
| --- | ------------------- | ------------------- | --------------------------------------------- |
| 1   | **Brainstorming**   | Fasilitator Kreatif | Mengeksplorasi ide, mengidentifikasi peluang  |
| 2   | **Product Brief**   | Business Analyst    | Mendefinisikan masalah, solusi, metrik sukses |
| 3   | **PRD**             | Product Manager     | Mendokumentasikan kebutuhan (FR/NFR)          |
| 4   | **Architecture**    | Software Architect  | Mendesain solusi teknis                       |
| 5   | **Epics & Stories** | Product Owner       | Membuat story yang siap implementasi          |

## Cara Penggunaan

### Langkah 1: Brainstorming

```
1. Siapkan Brainstorming Agent di platform AI
2. Berikan ide atau masalah awal
3. Ikuti sesi interaktif
4. Simpan output
```

### Langkah 2: Product Brief

```
1. Siapkan Product Brief Agent
2. Tempel output brainstorming
3. Jawab pertanyaan klarifikasi
4. Simpan output
```

### Langkah 3: PRD

```
1. Siapkan PRD Agent
2. Tempel Product Brief
3. Review kebutuhan dan prioritas
4. Simpan output
```

### Langkah 4: Architecture

```
1. Siapkan Architecture Agent
2. Tempel PRD
3. Diskusikan batasan dan keputusan teknis
4. Simpan output
```

### Langkah 5: Epics & Stories

```
1. Siapkan Epics & Stories Agent
2. Tempel PRD dan dokumen Architecture
3. Review struktur epic dan story
4. Simpan output → Siap untuk development!
```

## Setup Platform

Pilih platform yang Anda gunakan, lalu ikuti panduan lengkapnya:

| Platform | Panduan |
|----------|---------|
| Perplexity | [SETUP-PERPLEXITY.md](SETUP-PERPLEXITY.md) |
| Google Gemini | [SETUP-GEMINI.md](SETUP-GEMINI.md) |
| ChatGPT | [SETUP-CHATGPT.md](SETUP-CHATGPT.md) |

> **Tip:** Panduan di atas berisi langkah-langkah detail dengan gambar alur kerja, cocok untuk pemula.

## Fitur

- ✅ **Modular** - Gunakan agent mana saja secara standalone atau berurutan
- ✅ **Platform-agnostic** - Bisa digunakan di platform AI manapun
- ✅ **Semi-guided** - Ada checkpoint untuk validasi
- ✅ **Bahasa fleksibel** - Pilih bahasa output sesuai kebutuhan
- ✅ **Siap implementasi** - Output fokus pada APA, bukan BAGAIMANA

## File Supporting

Setiap agent memiliki file supporting dengan konteks tambahan:

| Agent           | File Supporting                         | Berisi                            |
| --------------- | --------------------------------------- | --------------------------------- |
| Brainstorming   | `01-brainstorming-techniques.md`        | SCAMPER, Six Hats, Mind Mapping   |
| Product Brief   | `02-product-brief-questions.md`         | Pertanyaan discovery, metrik      |
| PRD             | `03-prd-requirements-framework.md`      | Template FR/NFR, user stories     |
| Architecture    | `04-architecture-decision-framework.md` | Template ADR, evaluasi teknologi  |
| Epics & Stories | `05-epics-stories-guide.md`             | Penulisan story, APA vs BAGAIMANA |

Melampirkan file-file ini meningkatkan kualitas output, tapi opsional.

## Lisensi

MIT License - Bebas digunakan, dimodifikasi, dan dibagikan.

## Kontribusi

Kontribusi sangat diterima! Silakan:

- Tingkatkan efektivitas prompt
- Tambahkan materi supporting baru
- Perbaiki issue atau typo
- Bagikan pengalaman kamu
