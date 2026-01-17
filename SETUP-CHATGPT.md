# Cara Pakai Idea2Epic di ChatGPT

Panduan lengkap untuk mengubah ide menjadi Epic & Story menggunakan ChatGPT (Custom GPTs).

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

Di ChatGPT, Anda bisa membuat **Custom GPT** — yaitu AI dengan instruksi dan file referensi khusus yang bisa dipakai berulang kali.

> **Catatan:** Fitur Custom GPT memerlukan akun ChatGPT Plus.

### Langkah 1: Buka ChatGPT

1. Buka browser
2. Pergi ke [chatgpt.com](https://chatgpt.com)
3. Login dengan akun Anda

### Langkah 2: Buat GPT untuk Agent Pertama

1. Klik **"Explore GPTs"** di sidebar kiri
2. Klik **"Create"** (pojok kanan atas)
3. Pilih tab **"Configure"**
4. Isi **Name**: `Brainstorming Agent`
5. Isi **Description**: `Fasilitator brainstorming untuk eksplorasi ide`

### Langkah 3: Tambahkan Instruksi

1. Buka file `prompts/01-brainstorming-agent.md` di komputer Anda
2. **Salin semua isi file** tersebut
3. **Tempel** ke kotak **"Instructions"**

### Langkah 4: Tambahkan File Pendukung

1. Scroll ke bagian **"Knowledge"**
2. Klik **"Upload files"**
3. Upload file `supporting/01-brainstorming-techniques.md`
4. File ini akan menjadi referensi tambahan bagi AI

### Langkah 5: Simpan GPT

1. Scroll ke bawah, matikan **Web Browsing** dan **DALL-E** (tidak diperlukan)
2. Klik **"Create"**
3. Pilih **"Only me"** (atau "Anyone with a link" jika ingin berbagi)

GPT pertama Anda sudah siap!

### Langkah 6: Ulangi untuk 4 Agent Lainnya

Buat GPT baru untuk masing-masing:

| Nama GPT             | File Prompt                         | File Pendukung                              |
| -------------------- | ----------------------------------- | ------------------------------------------- |
| Product Brief Agent  | `prompts/02-product-brief-agent.md` | `supporting/02-product-brief-questions.md`  |
| PRD Agent            | `prompts/03-prd-agent.md`           | `supporting/03-prd-requirements-framework.md` |
| Architecture Agent   | `prompts/04-architecture-agent.md`  | `supporting/04-architecture-decision-framework.md` |
| Epics Stories Agent  | `prompts/05-epics-stories-agent.md` | `supporting/05-epics-stories-guide.md`      |

Setelah selesai, Anda punya 5 Custom GPTs yang siap dipakai kapan saja.

---

## Cara Pakai

### Tahap 1: Brainstorming

1. Klik **"Explore GPTs"** di sidebar
2. Klik tab **"My GPTs"**
3. Pilih **Brainstorming Agent**
4. Ketik ide Anda, contoh:
   > "Saya ingin membuat aplikasi untuk membantu UMKM mencatat keuangan"
5. Ikuti pertanyaan dari AI
6. Di akhir, AI akan membuat **dokumen brainstorming**
7. **Salin atau download dokumen tersebut** dan simpan

### Tahap 2: Product Brief

1. Kembali ke **"Explore GPTs"** → **"My GPTs"**
2. Pilih **Product Brief Agent**
3. Tempel dokumen brainstorming tadi
4. Ikuti pertanyaan dari AI
5. Di akhir, **salin atau download dokumen Product Brief** dan simpan

### Tahap 3: PRD

1. Kembali ke **"Explore GPTs"** → **"My GPTs"**
2. Pilih **PRD Agent**
3. Tempel dokumen Product Brief tadi
4. Ikuti pertanyaan dari AI
5. Di akhir, **salin atau download dokumen PRD** dan simpan

### Tahap 4: Architecture

1. Kembali ke **"Explore GPTs"** → **"My GPTs"**
2. Pilih **Architecture Agent**
3. Tempel dokumen PRD tadi
4. Ikuti pertanyaan dari AI
5. Di akhir, **salin atau download dokumen Architecture** dan simpan

### Tahap 5: Epics & Stories

1. Kembali ke **"Explore GPTs"** → **"My GPTs"**
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

### Keuntungan Pakai Custom GPT

- **Sekali setup, pakai selamanya** — tidak perlu tempel prompt lagi
- **File pendukung otomatis dipakai** — AI punya referensi lebih lengkap
- **Bisa dibagikan** — share link ke tim Anda
- **Bisa diedit** — kalau ada update prompt, tinggal edit GPT-nya

### Akses Cepat ke GPT Anda

- GPT yang sering dipakai akan muncul di sidebar kiri
- Atau akses langsung via **"Explore GPTs"** → **"My GPTs"**

### Kalau Bingung

- Setiap agent akan bertanya dulu sebelum lanjut
- Jawab saja dengan bahasa sehari-hari
- Kalau ada yang kurang jelas, tanya balik ke AI

### Kalau Mau Ulang dari Awal

- Klik **"New chat"** pada GPT yang sama
- Percakapan lama tetap tersimpan di history

---

## Tidak Punya ChatGPT Plus?

Anda tetap bisa pakai Idea2Epic dengan cara manual:

1. Buka chat baru di ChatGPT
2. Tempel isi file prompt di awal percakapan
3. Lampirkan file supporting sebagai attachment (ikon 📎)
4. Lanjutkan seperti biasa

Kekurangannya: Anda harus tempel prompt setiap mulai percakapan baru.
