# SignTalk - Penerjemah Bahasa Isyarat BISINDO

<p align="center">
  <img src="hutaw.png" alt="SignTalk Mascot / Hu Tao" width="200px">
</p>

**SignTalk** adalah aplikasi web interaktif yang menerjemahkan abjad bahasa isyarat BISINDO (Bahasa Isyarat Indonesia) secara real-time dari tangkapan kamera (webcam). Aplikasi ini menggunakan model *deep learning* berbasis **Keras 3** dan **TensorFlow** untuk melakukan klasifikasi citra abjad A sampai Z.

---

## ✨ Fitur Utama

*   📷 **Deteksi Kamera Real-Time:** Menangkap gerakan tangan langsung dari webcam pengguna dengan performa yang responsif.
*   🧠 **Model AI Presisi:** Didukung oleh model *EfficientNetV2* yang dioptimalkan untuk mengenali abjad BISINDO A-Z dengan akurasi tinggi.
*   ✍️ **Workspace Penerjemahan:** Menyusun huruf-huruf terdeteksi menjadi kata atau kalimat secara dinamis, lengkap dengan tombol spasi, hapus (backspace), dan bersihkan.
*   🔊 **Text-to-Speech (TTS):** Mengubah hasil terjemahan teks bahasa isyarat menjadi suara bahasa Indonesia secara langsung melalui browser.
*   📜 **Riwayat Huruf:** Menampilkan log hasil deteksi beserta tingkat kecocokan (confidence rate) dalam persentase.
*   📖 **Panduan Isyarat:** Menyediakan panduan praktis (kamus gambar/deskripsi) cara mengeja abjad BISINDO langsung di dalam aplikasi.

---

## 🛠️ Tech Stack

*   **Backend:** Python 3.10+, Flask, Flask-CORS
*   **Deep Learning:** Keras 3, TensorFlow (CPU version untuk hosting optimal)
*   **Frontend:** HTML5 (Semantic), Vanilla CSS, JavaScript (ES6+, Web Speech API, MediaDevices API)
*   **Server/Hosting:** Railway / Docker

---

## 🚀 Cara Menjalankan Secara Lokal

Ikuti langkah-langkah berikut untuk menjalankan SignTalk di komputer/laptop Anda:

### 1. Clone atau Unduh Project
Pastikan Anda sudah mengunduh folder project ini ke lokal.

### 2. Install Dependensi
Buka terminal/command prompt pada folder project, kemudian instal semua library yang diperlukan:
```bash
pip install -r requirements.txt
```

### 3. Jalankan Aplikasi
Jalankan file `app.py` untuk mengaktifkan server backend Flask:
```bash
python app.py
```

### 4. Akses Web App
Buka browser Anda dan akses alamat berikut:
```text
http://localhost:5000
```

---

## 🌐 Panduan Deployment di Railway

Proyek ini telah dikonfigurasi dengan [Procfile](Procfile) dan [requirements.txt](requirements.txt) agar siap di-deploy secara instan di **Railway.app**:

1.  Push proyek Anda ke GitHub.
2.  Masuk ke dashboard **Railway** dan klik **New Project** -> **Deploy from GitHub repo**.
3.  Pilih repository **signtalk** Anda.
4.  Tunggu hingga build selesai.
5.  Masuk ke tab **Settings** di Railway dan klik **Generate Domain** untuk mendapatkan link HTTPS.
6.  Aplikasi siap digunakan secara publik!
