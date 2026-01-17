# Cara Pakai Idea2Epic di Google Gemini

Panduan lengkap untuk mengubah ide menjadi Epic & Story menggunakan Google Gemini (Gems).

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

Di Gemini, Anda bisa membuat **Gems** — yaitu AI dengan instruksi dan file referensi khusus yang bisa dipakai berulang kali.

### Langkah 1: Buka Gemini

1. Buka browser
2. Pergi ke [gemini.google.com](https://gemini.google.com)
3. Login dengan akun Google Anda

### Langkah 2: Buat Gem untuk Agent Pertama

1. Klik **"Gem manager"** di sidebar kiri (ikon berlian 💎)
2. Klik **"New Gem"**
3. Isi **nama Gem**: `Brainstorming Agent`

### Langkah 3: Tambahkan Instruksi

1. Buka file `prompts/01-brainstorming-agent.md` di komputer Anda
2. **Salin semua isi file** tersebut
3. **Tempel** ke kotak **"Instructions"**

### Langkah 4: Tambahkan File Pendukung

1. Cari tombol **"Upload files"** atau ikon 📎
2. Upload file `supporting/01-brainstorming-techniques.md`
3. File ini akan menjadi referensi tambahan bagi AI
4. Klik **"Save"**

Gem pertama Anda sudah siap!

### Langkah 5: Ulangi untuk 4 Agent Lainnya

Buat Gem baru untuk masing-masing:

| Nama Gem             | File Prompt                         | File Pendukung                              |
| -------------------- | ----------------------------------- | ------------------------------------------- |
| Product Brief Agent  | `prompts/02-product-brief-agent.md` | `supporting/02-product-brief-questions.md`  |
| PRD Agent            | `prompts/03-prd-agent.md`           | `supporting/03-prd-requirements-framework.md` |
| Architecture Agent   | `prompts/04-architecture-agent.md`  | `supporting/04-architecture-decision-framework.md` |
| Epics Stories Agent  | `prompts/05-epics-stories-agent.md` | `supporting/05-epics-stories-guide.md`      |

Setelah selesai, Anda punya 5 Gems yang siap dipakai kapan saja.

---

## Cara Pakai

### Tahap 1: Brainstorming

1. Klik **"Gem manager"** di sidebar
2. Pilih **Brainstorming Agent**
3. Ketik ide Anda, contoh:
   > "Saya ingin membuat aplikasi untuk membantu UMKM mencatat keuangan"
4. Ikuti pertanyaan dari AI
5. Di akhir, AI akan membuat **dokumen brainstorming**
6. **Salin atau download dokumen tersebut** dan simpan

### Tahap 2: Product Brief

1. Kembali ke **Gem manager**
2. Pilih **Product Brief Agent**
3. Tempel dokumen brainstorming tadi
4. Ikuti pertanyaan dari AI
5. Di akhir, **salin atau download dokumen Product Brief** dan simpan

### Tahap 3: PRD

1. Kembali ke **Gem manager**
2. Pilih **PRD Agent**
3. Tempel dokumen Product Brief tadi
4. Ikuti pertanyaan dari AI
5. Di akhir, **salin atau download dokumen PRD** dan simpan

### Tahap 4: Architecture

1. Kembali ke **Gem manager**
2. Pilih **Architecture Agent**
3. Tempel dokumen PRD tadi
4. Ikuti pertanyaan dari AI
5. Di akhir, **salin atau download dokumen Architecture** dan simpan

### Tahap 5: Epics & Stories

1. Kembali ke **Gem manager**
2. Pilih **Epics Stories Agent**
3. Tempel dokumen PRD **dan** Architecture tadi
4. Ikuti pertanyaan dari AI
5. Di akhir, Anda mendapat **Epic & Story yang siap dikerjakan!**

---

## Tips

### Menyimpan Dokumen

Simpan setiap output ke file terpisah, contoh:
- `01-brainstorming.md`
- `02-product-brief.md`
- `03-prd.md`
- `04-architecture.md`
- `05-epics-stories.md`

### Keuntungan Pakai Gems

- **Sekali setup, pakai selamanya** — tidak perlu tempel prompt lagi
- **File pendukung otomatis dipakai** — AI punya referensi lebih lengkap
- **Mudah diakses** — tinggal pilih dari Gem manager
- **Bisa diedit** — kalau ada update prompt, tinggal edit Gem-nya

### Kalau Bingung

- Setiap agent akan bertanya dulu sebelum lanjut
- Jawab saja dengan bahasa sehari-hari
- Kalau ada yang kurang jelas, tanya balik ke AI

### Kalau Mau Ulang dari Awal

- Klik **"New chat"** pada Gem yang sama
- Atau buat percakapan baru dari Gem manager
