# 🏭 Live SCADA Monitoring: Smart Cement Silo System

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23F7DF1E.svg?style=for-the-badge&logo=javascript&logoColor=black)
![Industry 4.0](https://img.shields.io/badge/Industry_4.0-Automation-blue?style=for-the-badge)

Repositori ini berisi kode sumber untuk **Simulator Smart Cement Silo v3.0**, sebuah visualisasi *dashboard* berbasis web interaktif yang mengadopsi prinsip antarmuka SCADA (*Supervisory Control and Data Acquisition*). Proyek ini dirancang untuk mensimulasikan penerapan arsitektur *Control Loop* terintegrasi pada fase penyimpanan produk akhir industri semen menggunakan kombinasi instrumen inti unggulan dari **VEGA Grieshaber KG** dan sensor pelengkap lingkungan.

---

## 🎨 Presentasi Proyek & Desain UI
Alur pemikiran rekayasa (*engineering workflow*), detail justifikasi finansial (ROI), arsitektur sistem otomatisasi, serta perancangan desain visual untuk proyek interaktif ini dapat diakses secara komprehensif melalui tautan berikut:
🔗 **[Desain Proyek Smart Silo - Canva Presentation](https://canva.link/kfjyrrbrmoau1uq)**

---

## ⚙️ Fitur Otomatisasi & Loop Pengendalian
Simulator ini mengintegrasikan 3 pilar utama otomasi industri (Loop Tertutup) yang bekerja secara dinamis dan real-time:

1. **Monitoring (Sensor / Inputs)**
   * **VEGAPULS 6X (Radar Level):** Mengukur tingkat volume semen kontinu menembus debu pekat menggunakan teknologi 80 GHz.
   * **VEGAWAVE 62 (Vibrating Limit Switch):** Sensor batas atas mekanis (*Overfill Protection*).
   * **VEGABAR 82 (Pressure Transmitter):** Memantau tekanan corong bawah (*hopper*) dengan sel keramik `CERTEC®` tahan abrasi.
   * **Air Moisture Sensor:** Mendeteksi kelembapan udara instrumen penyuplai kompresor.
   * **Triboelectric Dust Sensor:** Memantau tingkat kepekatan emisi debu pada bagian *baghouse filter* atap silo.

2. **Controlling (PLC / DCS Logic State)**
   * Sistem otomatisasi mengevaluasi *setpoint* bahaya secara simultan dan mampu mengeluarkan pesan kedaruratan berlapis (*multiple alarms*).

3. **Actuator (Outputs / Execution)**
   * **Infeed Valve:** Menutup paksa pengisian aliran semen secara otomatis saat kondisi kritis pengisian berlebih terpicu.
   * **Blower Fluidisasi:** Berhenti otomatis jika tekanan melonjak atau jika udara kompresor terlalu lembap untuk mencegah kegagalan mekanis.
   * **Sistem Purge Filter:** Melakukan pembersihan udara bertekanan darurat apabila emisi debu melewati batas baku mutu lingkungan.

---

## 📈 Skenario Visual Interaktif yang Dapat Diuji
* **Simulasi Semen Membatu (*Caking/Coatings*):** Naikkan slider kelembapan udara (> 60 %RH), semen secara visual akan berubah warna kusam, dan PLC memutus kerja *blower* demi mencegah semen membatu.
* **Simulasi Filter Atap Jebol:** Geser emisi debu melewati batas regulasi (> 50 mg/m³), awan polusi partikulat di puncak silo akan menebal dan memicu katup pembersih (*purge system*).
* **Simulasi Overfill (Silo Luber):** Geser tingkat pengisian semen hingga titik ekstrem (> 95%), garpu tala sensor akan terendam kaku, memicu interlock pengaman, dan menutup paksa katup pengisian.

---

## 🚀 Cara Menjalankan Simulator Secara Lokal

Aplikasi web ini dibangun murni menggunakan **Vanilla JavaScript, HTML5, dan CSS3** tanpa memerlukan *dependency* atau *framework* eksternal (sangat ringan dan kompatibel).

1. Unduh atau klon repositori ini:
   ```bash
   git clone [https://github.com/username-anda/nama-repositori.git](https://github.com/username-anda/nama-repositori.git)
