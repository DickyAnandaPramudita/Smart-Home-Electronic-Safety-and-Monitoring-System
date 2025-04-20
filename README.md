# # 🏠 Smart-Home Electronic Safety and Monitoring System

Proyek ini bertujuan untuk mengembangkan sistem automasi untuk Smart Home, menggunakan komponen utama seperti Arduino Mega, ACS712, ZMPT1010B dan berbagai sensor. Arduino mega bertindak sebagai mikroprosesor utama yang mengontrol komunikasi antar sensor dan perangkat, memungkinkan pemantauan dan pengontrolan secara real-time melalui jaringan UART TTL. Sistem ini dilengkapi dengan Auto cutt-off untuk menjaga alat elektronik rumah dari fluktuasi tegangan jala-jala PLN.

Untuk memantau konsumsi energi, digunakan sensor arus ACS712 dan sensor tegangan ZMPT101B yang secara akurat mengukur penggunaan arus listrik dan tegangan pada berbagai perangkat. Selain itu, Relay SPDT berfungsi sebagai saklar otomatis yang memungkinkan pengendalian perangkat elektronik seperti lampu.
## 📌 Fitur Utama

- 🔥 **Deteksi Suhu dan Kebakaran**: Menggunakan sensor suhu (seperti DHT22/LM35) untuk mendeteksi suhu abnormal yang berpotensi menyebabkan kebakaran.
- 🛑 **Deteksi Gas Berbahaya**: Sensor gas (seperti MQ-2/MQ-135) mendeteksi adanya kebocoran gas LPG atau asap.
- 👁️ **Pemantauan Kehadiran**: Sensor PIR untuk mendeteksi pergerakan mencurigakan saat rumah dalam kondisi kosong.
- 💡 **Kontrol Perangkat Elektronik**: Otomatisasi lampu, kipas, dan alat elektronik lain berdasarkan kondisi lingkungan.
- 📟 **Antarmuka LCD / Web Monitoring**: Menampilkan status sensor secara real-time melalui LCD atau dashboard monitoring berbasis Python GUI / web.
- 📱 **Pemberitahuan Darurat**: Opsional untuk mengirim notifikasi ke HP atau email menggunakan modul tambahan (ESP8266 / GSM).

## 🧰 Teknologi dan Tools

- 🖥️ **Mikrokontroler**: Arduino (Uno/Nano)
- 🔌 **Sensor**: DHT22, MQ-2, PIR, Flame sensor, Sensor level air
- 📊 **Interface**: LCD I2C 16x2 / GUI Python (Tkinter) / Web (Flask - opsional)
- 🔁 **Komunikasi**: UART Serial, RF/ESP jika menggunakan jaringan
- ⚙️ **Bahasa Pemrograman**: Arduino C++, Python

## 🔧 Cara Kerja

1. Sensor-sensor aktif membaca kondisi lingkungan.
2. Data dikirim ke mikrokontroler.
3. Mikrokontroler memproses data dan mengambil aksi:
   - Menghidupkan buzzer jika terdeteksi bahaya.
   - Menampilkan data ke LCD atau GUI.
   - Mengaktifkan atau menonaktifkan perangkat elektronik.
4. (Opsional) Kirim notifikasi ke pemilik rumah melalui jaringan.

## 📷 Dokumentasi / Demo

> Tambahkan gambar skematik, foto alat, atau video demo jika tersedia di sini.

## 🚀 Cara Menjalankan

### 1. Arduino
- Upload kode ke Arduino melalui Arduino IDE.
- Sambungkan sensor ke pin yang sesuai.

### 2. Python GUI (opsional)
```bash
pip install pyserial tkinter
python monitoring_gui.py
