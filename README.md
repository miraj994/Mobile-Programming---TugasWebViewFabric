# 📱 Tugas WebView Fabric — Portal Kampus

Aplikasi mobile sederhana berbasis **React Native** yang menampilkan website portal akademik (SIAKAD) kampus langsung di dalam aplikasi menggunakan komponen **WebView**. Proyek ini dibuat untuk tugas mata kuliah **Mobile Programming**, sekaligus untuk mencoba **New Architecture (Fabric)** milik React Native.

## 🎯 Deskripsi Proyek

Mahasiswa biasanya membuka SIAKAD lewat browser. Aplikasi ini membungkus halaman login SIAKAD ke dalam tampilan aplikasi native, sehingga akses ke portal kampus terasa seperti membuka aplikasi biasa, lengkap dengan header dan indikator loading.

Repository ini juga berisi versi pembanding yang dibuat dengan **MIT App Inventor**, supaya bisa dilihat perbedaan cara membuat WebView lewat kode (React Native) dan lewat block programming (App Inventor).

## ✨ Fitur Utama

- 🌐 Menampilkan halaman login SIAKAD (`siakad.unla.ac.id`) di dalam aplikasi menggunakan `react-native-webview`
- 🧭 Header aplikasi dengan judul **"Portal Kampus - Fabric WebView"**
- ⏳ Indikator loading otomatis saat halaman sedang dimuat (`startInLoadingState`)
- ⚙️ JavaScript aktif di dalam WebView sehingga form login dan fitur portal bisa berjalan
- 🧱 Menggunakan **New Architecture (Fabric)**, aktif lewat `newArchEnabled=true`
- 📲 Mendukung Android dan iOS
- 🧩 Versi App Inventor dengan tombol **HOME** dan **REFRESH** (folder `MIT_App_Inventor`)

## 🛠️ Teknologi yang Digunakan

| Kategori | Teknologi |
| --- | --- |
| Framework | React Native 0.87.1 |
| Bahasa | TypeScript, Kotlin (Android), Swift (iOS) |
| Library UI | React 19, `react-native-webview`, `react-native-safe-area-context` |
| Build Tool | Metro Bundler, Gradle, CocoaPods |
| JS Engine | Hermes |
| Testing & Lint | Jest, ESLint, Prettier |
| Pembanding | MIT App Inventor |

## 📂 Struktur Folder

```
Mobile-Programming---TugasWebViewFabric/
├── App.tsx               # Tampilan utama (header + WebView)
├── index.js              # Entry point aplikasi
├── android/              # Project native Android
├── ios/                  # Project native iOS
├── MIT_App_Inventor/     # Versi App Inventor (WebView.aia & WebView.apk)
├── __tests__/            # File pengujian
└── package.json          # Daftar dependency dan script
```

## 🚀 Cara Instalasi & Menjalankan

### Prasyarat

- [Node.js](https://nodejs.org/) versi **22.11 atau lebih baru**
- Android Studio (untuk Android) atau Xcode (untuk iOS)
- Sudah menyelesaikan [Set Up Your Environment](https://reactnative.dev/docs/set-up-your-environment) dari dokumentasi React Native

### Langkah-langkah

**1. Clone repository**

```bash
git clone https://github.com/miraj994/Mobile-Programming---TugasWebViewFabric.git
cd Mobile-Programming---TugasWebViewFabric
```

**2. Install dependency**

```bash
npm install
```

**3. Jalankan Metro (biarkan terminal ini tetap terbuka)**

```bash
npm start
```

**4. Jalankan aplikasi** (buka terminal baru)

```bash
# Android (emulator atau HP yang tersambung)
npm run android

# iOS (hanya di macOS)
bundle install            # pertama kali saja
cd ios && bundle exec pod install && cd ..
npm run ios
```

### Mencoba Versi App Inventor

Folder `MIT_App_Inventor` berisi dua file:

- `WebView.apk` — bisa langsung diinstal di HP Android
- `WebView.aia` — bisa diimpor ke [MIT App Inventor](https://appinventor.mit.edu/) lewat menu **Projects → Import project (.aia)**

## 📸 Tangkapan Layar / Demo

<img width="598" height="1280" alt="WhatsApp Image 2026-11-13 at 13 06 05" src="https://github.com/user-attachments/assets/49f915ed-c271-409b-8d49-b3b895abeb94" />


## 🧪 Menjalankan Test & Lint

```bash
npm test      # menjalankan Jest
npm run lint  # memeriksa gaya penulisan kode dengan ESLint
```

## 👤 Pembuat

**Miraj Jamal Sidik**
Mahasiswa Informatika, Universitas Langlangbuana
Mata kuliah: Mobile Programming

[GitHub: @miraj994](https://github.com/miraj994)

## 📄 Catatan

Proyek ini dibuat untuk keperluan pembelajaran. Halaman SIAKAD yang ditampilkan adalah milik pihak kampus, dan aplikasi ini tidak menyimpan data login pengguna.
