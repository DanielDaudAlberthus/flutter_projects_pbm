# Praktikum PBM Navigasi Flutter
---

## Gambaran Singkat Jenis Navigasi

### 1. Named Routes
**Named Routes** memungkinkan navigasi antar layar menggunakan nama rute yang telah didefinisikan di awal aplikasi. Cocok untuk aplikasi dengan banyak layar dan kebutuhan navigasi yang konsisten.

- **Contoh Widget:**  
  - `MaterialApp(routes: {...})`
  - `Navigator.pushNamed(context, '/detail')`

---

### 2. Navigator 2.0
**Navigator 2.0** menawarkan kontrol penuh terhadap stack navigasi menggunakan deklaratif pages dan RouteInformationParser. Cocok untuk aplikasi yang membutuhkan navigasi dinamis dan integrasi dengan browser (web).

- **Contoh Widget:**  
  - `Navigator(pages: [...], onPopPage: ...)`
  - `MaterialPage`
  - Custom `RouteInformationParser` dan `RouterDelegate`

---

### 3. Nested Navigation
**Nested Navigation** digunakan ketika aplikasi memiliki alur atau flow yang kompleks di dalam satu layar, seperti wizard atau multi-step setup. Menggunakan navigator bersarang (nested navigator) untuk mengelola sub-rute secara terpisah dari navigator utama.

- **Contoh Widget:**  
  - `Navigator(key: ..., initialRoute: ..., onGenerateRoute: ...)`
  - Widget custom seperti `SetupFlowScreen`

---

### 4. Deep Linking
**Deep Linking** memungkinkan aplikasi untuk membuka layar tertentu berdasarkan URL eksternal atau internal, sehingga pengguna dapat langsung diarahkan ke konten spesifik. Biasanya diimplementasikan dengan Navigator 2.0.

- **Contoh Widget:**  
  - `MaterialApp.router`
  - Custom `RouteInformationParser` dan `RouterDelegate`
  - Mendukung URL seperti `/detail/1` atau `/settings`

---

## Tangkapan Layar & Keterangan

> **Catatan:** Silakan tambahkan tangkapan layar aplikasi Anda di bawah ini. Setiap gambar diberi keterangan dan dijelaskan widget utama yang tampil.

### 1. Named Routes

[HomeScreen - Named Routes]![image](https://github.com/user-attachments/assets/a3db30c0-c0c4-440b-b4b2-8ed660a70d67)

**Keterangan:** Tampilan `HomeScreen` dengan tombol navigasi ke Detail, Settings, dan About. Menggunakan widget `Scaffold`, `ElevatedButton`.

![AboutScreen - Named Routes]![image](https://github.com/user-attachments/assets/a91a8000-d9d8-4b2c-898e-9910fa67eabb)

**Keterangan:** Tampilan `AboutScreen` yang diakses melalui named route `/about`. Menggunakan widget `Scaffold`, `Text`, `ElevatedButton`.

---

### 2. Navigator 2.0

[HomeScreen - Navigator 2.0]![image](https://github.com/user-attachments/assets/176170ab-3b20-46b7-b7bf-27cbd4aea0fb)

**Keterangan:** Daftar item pada `HomeScreen`. Menggunakan widget `ListView`, `ListTile`.

[DetailScreen - Navigator 2.0]![image](https://github.com/user-attachments/assets/9e6625bf-5e0d-44cf-9e79-4d6c942f770e)

**Keterangan:** Tampilan detail item dengan field `description`. Menggunakan widget `Text`, `ElevatedButton`.

---

### 3. Nested Navigation

[HomeScreen - Nested Navigation]![image](https://github.com/user-attachments/assets/aa1560c6-19b7-4059-b713-055a293f5523)

**Keterangan:** Tampilan utama aplikasi. Menggunakan widget `Scaffold`, `ElevatedButton`.

[SetupFlowScreen - Nested Navigation]![image](https://github.com/user-attachments/assets/1fba7ff2-c028-4ca7-a14e-d402404de259)
 
**Keterangan:** Alur setup dengan navigator bersarang. Widget utama: `SetupFlowScreen`, `Navigator`, `FindDevicesScreen`, `ConnectDeviceScreen`, `ConfirmDeviceScreen`.

---

### 4. Deep Linking

[Screen - Deep Linking]![image](https://github.com/user-attachments/assets/f8ec27cc-f4bf-4516-8011-c8f009fad189)

**Keterangan:** Tampilan utama dengan daftar item dan tombol Settings. Widget utama: `HomeScreen`, `ListView`, `IconButton`.

[SettingsScreen - Deep Linking]![image](https://github.com/user-attachments/assets/898e0a38-a28d-4dcc-920b-fb4aaeca7dd3)

**Keterangan:** Tampilan `SettingsScreen` yang dapat diakses melalui deep link `/settings`. Widget utama: `SettingsScreen`, `Scaffold`, `Text`.

---
