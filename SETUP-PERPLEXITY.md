# Cara Pakai Idea2Epic di Perplexity

Panduan lengkap untuk mengubah ide menjadi Epic & Story menggunakan Perplexity Spaces.

---

## Alur Kerja

```
   IDE AWAL
      │
      ▼
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│ 1. Brain-   │────▶│ 2. Product  │────▶│ 3. PRD      │
│    storming │     │    Brief    │     │             │
└─────────────┘     └─────────────┘     └─────────────┘
                                               │
                    ┌──────────────────────────┘
                    ▼
             ┌─────────────┐     ┌─────────────┐
             │ 4. Archi-   │────▶│ 5. Epics &  │────▶  SIAP DEVELOP!
             │    tecture  │     │    Stories  │
             └─────────────┘     └─────────────┘
```

**Setiap agent punya tugas berbeda:**

| Agent              | Fungsi                          |
| ------------------ | ------------------------------- |
| 1. Brainstorming   | Eksplorasi ide, cari peluang    |
| 2. Product Brief   | Definisikan masalah & solusi    |
| 3. PRD             | Tulis kebutuhan lengkap         |
| 4. Architecture    | Desain teknis                   |
| 5. Epics & Stories | Pecah jadi task siap dikerjakan |

---

## Persiapan (Sekali Saja)

Di Perplexity, Anda bisa membuat **Spaces** — yaitu ruang kerja dengan instruksi dan file referensi yang bisa dipakai berulang kali.

### Langkah 1: Buka Perplexity

1. Buka browser
2. Pergi ke [perplexity.ai](https://perplexity.ai)
3. Login atau buat akun

### Langkah 2: Buat Space untuk Agent Pertama

1. Klik **"Spaces"** di sidebar kiri
2. Klik **"Create Space"**
3. Isi **nama Space**: `Brainstorming Agent`
4. Klik **"Create"**

### Langkah 3: Tambahkan Instruksi

1. Di dalam Space, klik **"Customize"** atau ikon gear ⚙️
2. Buka file `prompts/01-brainstorming-agent.md` di komputer Anda
3. **Salin semua isi file** tersebut
4. **Tempel** ke kotak **"Instructions"**
5. Klik **"Save"**

### Langkah 4: Tambahkan File Pendukung

1. Masih di halaman Space, cari tombol **"Add Files"** atau **"Upload"**
2. Upload file `supporting/01-brainstorming-techniques.md`
3. File ini akan menjadi referensi tambahan bagi AI

### Langkah 5: Ulangi untuk 4 Agent Lainnya

Buat Space baru untuk masing-masing:

| Nama Space           | File Prompt                         | File Pendukung                              |
| -------------------- | ----------------------------------- | ------------------------------------------- |
| Product Brief Agent  | `prompts/02-product-brief-agent.md` | `supporting/02-product-brief-questions.md`  |
| PRD Agent            | `prompts/03-prd-agent.md`           | `supporting/03-prd-requirements-framework.md` |
| Architecture Agent   | `prompts/04-architecture-agent.md`  | `supporting/04-architecture-decision-framework.md` |
| Epics Stories Agent  | `prompts/05-epics-stories-agent.md` | `supporting/05-epics-stories-guide.md`      |

Setelah selesai, Anda punya 5 Spaces yang siap dipakai kapan saja.

---

## Cara Pakai

### Tahap 1: Brainstorming

1. Buka **Spaces** di sidebar
2. Pilih **Brainstorming Agent**
3. Ketik ide Anda, contoh:
   > "Saya ingin membuat aplikasi untuk membantu UMKM mencatat keuangan"
4. Ikuti pertanyaan dari AI
5. Di akhir, AI akan membuat **dokumen brainstorming**
6. **Salin atau download dokumen tersebut** dan simpan

### Tahap 2: Product Brief

1. Buka **Spaces** → pilih **Product Brief Agent**
2. Tempel dokumen brainstorming tadi
3. Ikuti pertanyaan dari AI
4. Di akhir, **salin atau download dokumen Product Brief** dan simpan

### Tahap 3: PRD

1. Buka **Spaces** → pilih **PRD Agent**
2. Tempel dokumen Product Brief tadi
3. Ikuti pertanyaan dari AI
4. Di akhir, **salin atau download dokumen PRD** dan simpan

### Tahap 4: Architecture

1. Buka **Spaces** → pilih **Architecture Agent**
2. Tempel dokumen PRD tadi
3. Ikuti pertanyaan dari AI
4. Di akhir, **salin atau download dokumen Architecture** dan simpan

### Tahap 5: Epics & Stories

1. Buka **Spaces** → pilih **Epics Stories Agent**
2. Tempel dokumen PRD **dan** Architecture tadi
3. Ikuti pertanyaan dari AI
4. Di akhir, Anda mendapat **Epic & Story yang siap dikerjakan!**

---

## Tips

### Menyimpan Dokumen

Simpan setiap output ke file terpisah, contoh:
- `01-brainstorming.md`
- `02-product-brief.md`
- `03-prd.md`
- `04-architecture.md`
- `05-epics-stories.md`

### Keuntungan Pakai Spaces

- **Sekali setup, pakai selamanya** — tidak perlu tempel prompt lagi
- **File pendukung otomatis dipakai** — AI punya referensi lebih lengkap
- **Bisa diakses dari mana saja** — tinggal buka Spaces

### Kalau Bingung

- Setiap agent akan bertanya dulu sebelum lanjut
- Jawab saja dengan bahasa sehari-hari
- Kalau ada yang kurang jelas, tanya balik ke AI

### Kalau Mau Ulang dari Awal

- Klik **"New Thread"** di dalam Space yang sama
- Percakapan lama tetap tersimpan
