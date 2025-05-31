# 🎨 Stok Bengkel Pintar - Frontend App

![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Ant Design](https://img.shields.io/badge/Ant%20Design-0170FE?style=for-the-badge&logo=antdesign&logoColor=white)
![MUI](https://img.shields.io/badge/MUI-007FFF?style=for-the-badge&logo=mui&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)

---

## 📄 Deskripsi Proyek

Proyek ini adalah *frontend* aplikasi **Stok Bengkel Pintar**, antarmuka pengguna yang berinteraksi dengan **Backend API Laravel** kita. Aplikasi ini memungkinkan bengkel mengelola stok mereka, melakukan transaksi, dan melihat ringkasan data penting.

Dibangun menggunakan **React** (dengan Vite sebagai *bundler*) dan didukung oleh komponen UI dari **Ant Design** atau **MUI**.

---

## 🛠️ Persyaratan Sistem

Pastikan sistem Anda memenuhi persyaratan berikut untuk menjalankan proyek ini secara lokal:

* **Node.js:** >= 14.x (disarankan versi LTS terbaru)
* **npm:** (biasanya sudah termasuk dengan Node.js) atau **Yarn**
* **Git:** Untuk manajemen kode.
* **Backend API:** Pastikan *backend* API Laravel sudah berjalan di lokal Anda atau di server pengembangan yang dapat diakses.

---

## ⚙️ Panduan Setup Lokal

Ikuti langkah-langkah di bawah ini untuk menjalankan proyek *frontend* di lingkungan lokal Anda.

1.  **Clone Repository:**
    ```bash
    git clone [https://github.com/your-username/stok-bengkel-app.git](https://github.com/your-username/stok-bengkel-app.git)
    cd stok-bengkel-app
    ```
    *(Ganti `your-username` dengan username GitHub Anda)*

2.  **Instal Dependensi Node.js:**
    ```bash
    npm install
    # atau jika Anda menggunakan yarn
    # yarn install
    ```

3.  **Konfigurasi Environment:**
    * Buat file `.env.local` dari contoh `.env.example` (jika ada) atau buat manual:
        ```
        VITE_API_BASE_URL=http://localhost:8000/api # Ganti dengan URL API Backend Anda
        ```
    * Pastikan `VITE_API_BASE_URL` mengarah ke *endpoint* API *backend* Laravel Anda. Jika Anda menjalankan *backend* di port `8000`, maka URL di atas sudah benar.

4.  **Jalankan Aplikasi:**
    ```bash
    npm run dev
    # atau jika Anda menggunakan yarn
    # yarn dev
    ```
    Aplikasi *frontend* Anda sekarang akan berjalan di `http://localhost:5173` (port default Vite) atau port lain yang ditunjukkan di terminal.

---

## ⚡ Fitur Utama (MVP)

* **Autentikasi:** *Login* dan *Register* *user* baru.
* **Manajemen Produk:** Melihat daftar stok, menambah produk baru.
* **Manajemen Transaksi:** Mencatat transaksi masuk/keluar/retur/rusak.
* **Dashboard Sederhana:** Menampilkan produk terlaris.

---

## 🌳 Panduan Git Branching untuk Kolaborasi

Kita akan menggunakan modifikasi dari **Git Flow sederhana** yang cocok untuk tim kecil kita. Tujuannya adalah menjaga *codebase* tetap bersih, stabil, dan memungkinkan kita bekerja secara paralel tanpa saling menimpa pekerjaan.

### 📚 Branch Utama

* **`main` (atau `master`):**
    * Ini adalah *branch* yang **selalu stabil** dan mencerminkan *code* yang sudah di-*deploy* ke *production* (atau siap *deploy*).
    * **JANGAN PERNAH *COMMIT* LANGSUNG KE `main`!**
    * Perubahan hanya masuk ke `main` melalui **Pull Request (PR)** dari `develop` setelah *review* dan *testing* menyeluruh.

* **`develop`:**
    * Ini adalah *branch* utama untuk **pengembangan aktif**.
    * Semua fitur baru dan perbaikan *bug* akan digabungkan ke sini.
    * `develop` harus selalu dalam keadaan yang relatif stabil dan dapat diuji.

### 🌱 Branch Fitur (Feature Branches)

* Setiap kali Anda atau anggota tim memulai sebuah *task* baru (dari GitHub Project Board), Anda harus membuat **`feature branch`** terpisah dari `develop`.
* **Konvensi Penamaan:** `feature/[deskripsi-singkat-task]` atau `feature/[nomor-issue-github]-[deskripsi-singkat]`
    * Contoh: `feature/frontend-login-ui`, `feature/1.11-login-register-components`, `feature/2.6-product-list-page`
* **Cara Membuat:**
    ```bash
    git checkout develop
    git pull origin develop # Pastikan develop Anda yang terbaru
    git checkout -b feature/[nama-branch-anda]
    ```
* **Tujuan:** Mengisolasi pekerjaan Anda sehingga tidak mengganggu pekerjaan orang lain atau *codebase* utama sampai *task* Anda selesai dan siap digabungkan.

### 🚀 Proses Kerja Harian (Workflow)

1.  **Ambil Task:**
    * Pilih satu *task* dari kolom **"To Do"** di GitHub Project Board kita.
    * *Assign* *task* tersebut ke diri Anda di GitHub.
    * Pindahkan *card* *task* tersebut ke kolom **"In Progress"**.

2.  **Buat Feature Branch:**
    * Pastikan `develop` *branch* lokal Anda yang terbaru: `git checkout develop && git pull origin develop`
    * Buat *feature branch* baru sesuai konvensi penamaan: `git checkout -b feature/[nama-task-anda]`

3.  **Coding & Commit:**
    * Kerjakan *task* Anda di *feature branch* ini.
    * Lakukan *commit* secara berkala dengan pesan *commit* yang jelas dan deskriptif. Jika memungkinkan, referensikan nomor *issue* GitHub.
        ```bash
        git add .
        git commit -m "feat: Menambahkan halaman login UI #1.11"
        ```

4.  **Push ke Remote:**
    * Setelah selesai atau di akhir sesi *coding*, *push* *feature branch* Anda ke *remote* (GitHub):
        ```bash
        git push origin feature/[nama-task-anda]
        ```

5.  **Buat Pull Request (PR):**
    * Setelah *task* selesai dan *code* Anda siap untuk di-*review*, buka GitHub dan buat **Pull Request (PR)** dari *feature branch* Anda ke *target branch* **`develop`**.
    * Berikan deskripsi PR yang jelas tentang apa yang Anda kerjakan, mengapa, dan bagaimana pengujiannya.
    * **Assign** PR ke rekan tim untuk *review* (jika ada).
    * *Link* PR ke *issue* GitHub yang relevan.
    * Pindahkan *card* *task* di Project Board ke kolom **"In Review"** (jika ada) atau tetap di "In Progress" sampai di-*review*.

6.  **Code Review:**
    * Rekan tim akan meninjau *code* Anda, memberikan komentar, dan mungkin meminta perubahan.
    * Diskusikan *feedback* dan lakukan revisi yang diperlukan.

7.  **Merge PR:**
    * Setelah PR disetujui (minimal 1 *approval*), *merge* *feature branch* ke `develop`. Gunakan opsi **"Squash and merge"** jika ingin riwayat *commit* yang lebih bersih di `develop`.
    * **Pindahkan *card* *task* di Project Board ke kolom "Done".**

8.  **Hapus Feature Branch Lokal & Remote:**
    * Setelah *merge*, hapus *feature branch* lokal Anda: `git branch -d feature/[nama-task-anda]`
    * Hapus juga *feature branch* di *remote*: `git push origin --delete feature/[nama-task-anda]`

---

## 🤝 Kontribusi

Kami sangat menghargai kontribusi Anda! Ikuti panduan *branching* di atas dan jangan ragu untuk membuat *issue* baru jika Anda menemukan *bug* atau memiliki ide fitur.

---
