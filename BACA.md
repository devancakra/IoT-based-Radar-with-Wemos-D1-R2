[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/IoT-based-Radar-with-Wemos-D1-R2)
![IoT](https://img.shields.io/badge/Project-Internet%20of%20Things-blue?logo=arduino&color=%23F7DF1E)

# IoT-based-Radar-with-Wemos-D1-R2
<strong>Tugas Akhir UCI Coursera 2023</strong><br><br>
Proyek ini sangat erat kaitannya dengan teknologi pertahanan, dimana alat ini digunakan untuk mendeteksi ada atau tidaknya objek di sekitar area yang telah ditentukan. Sistem pertahanan ini dijalankan dengan protokol MQTT. Selain itu, sistem ini juga menyediakan user interface untuk mempermudah pemantauan.

<br><br>

## Fitur / Kerangka Kerja / Alat
| Media | Deskripsi |
| --- | --- |
| Papan Pengembangan | Wemos D1 R2 |
| Editor Kode | Arduino IDE & Processing |
| Driver | USB-Serial CH340 |
| Platform IoT | mosquitto |
| Peralatan IoT | MQTT Explorer |
| Protokol IoT | MQTT |
| Arsitektur IoT | 3 Lapisan |
| Bahasa Pemrograman | C/C++ dan Python |
| Pustaka Arduino | ESP8266WiFi, Servo, PubSubClient, ArduinoJson |
| Aktuator | Motor Servo SG90 180° (x1) |
| Sensor | HC-SR04: Sensor Ultrasonik (x1) |
| Komponen Lainnya | Kabel micro usb (x1), Kabel jumper, DLL |

<br><br>

## Unduh & Instal
1. Arduino IDE
   
   ```
   https://www.arduino.cc/en/software
   ```
   <br>
   
2. Processing
   
   ```
   https://processing.org/download
   ```
   <br>

3. MQTT Explorer
   
   ```
   https://mqtt-explorer.com/
   ```
   <br>
   
4. USB-Serial CH340

   ```
   https://bit.ly/CH340_Driver
   ```
   
<br><br>

## Skema Alur Sistem
Ketika sebuah objek berada di area deteksi sensor, maka sensor akan merespon dengan mengirimkan data publish ke platform IoT (mosquito) dan kemudian mengirimkan kembali dalam bentuk data subscribe untuk ditampilkan pada serial monitor. Sedangkan pada grafik, pengguna juga dapat melihat perbedaan warna yang signifikan pada area deteksi. Jika tidak ada objek yang ditemukan, sensor dan aktuator akan selalu siaga.

<br><br>

## Persyaratan Proyek
<table>
<tr>
<th width="420">Diagram Blok</th>
<th width="420">Diagram Ilustrasi</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/b9890292-0b28-4a78-8f9d-39df8f806177" alt="Block-Diagram"></td>
<td><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/183c9c9e-eb51-4b88-945b-d30ddc97833a" alt="Pictorial-Diagram"></td>
</tr>
</table>
<table>
<tr>
<th width="840">Pengkabelan</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/e49d2460-5653-4fe2-8c6d-0668844efd1f" alt="Wiring"></td>
</tr>
</table>

<br><br>

## Pengaturan Arduino IDE
1. Buka ``` Arduino IDE ``` terlebih dahulu, kemudian buka proyek Wemos D1 R2 Radar dengan cara klik: ``` File ``` -> ``` Open ``` -> ``` wemos_d1r2_radar.ino ```.<br><br>
   
2. Isi ``` Url Pengelola Papan Tambahan ``` di Arduino IDE<br><br>
   • Cara: klik ``` File ``` -> ``` Preferences ``` -> masukkan ``` Boards Manager Url ``` dengan menyalin tautan berikut:
   
   ```
   http://arduino.esp8266.com/stable/package_esp8266com_index.json
   ```
   
3. ``` Pengaturan Board ``` di Arduino IDE<br><br>
   • Cara: klik ``` Tools ``` -> ``` Board ``` -> ``` Boards Manager ``` -> Instal ``` esp8266 ```. Kemudian pilih Board dengan mengklik: ``` Tools ``` -> ``` Board ``` -> ``` ESP8266 Board ``` -> ``` LOLIN(WEMOS) D1 R2 & mini ```.
   <br><br>
   
4. ``` Ubah Kecepatan Papan ``` di Arduino IDE<br><br>
   • Cara: klik ``` Tools ``` -> ``` Upload Speed ``` -> ``` 115200 ```.
   <br><br>
   
5. ``` Instal Pustaka ``` di Arduino IDE<br><br>
   • Cara: unduh semua file zip pustaka. Kemudian tempelkan di: ``` C:\Users\Computer_Username\Documents\Arduino\libraries ```.
   <br><br>

6. ``` Pengaturan Port ``` di Arduino IDE<br><br>
   • Cara: klik ``` Port ``` -> Pilih sesuai dengan port perangkat Anda ``` (Anda dapat melihatnya di Device Manager) ```.
   <br><br>

7. Ubah ``` Nama WiFi ```, ``` Kata Sandi WiFi ```, dan ``` ID Klien ``` sesuai dengan yang Anda gunakan saat ini.<br><br>

8. Sebelum mengunggah program, silakan klik: ``` Verify ```.<br><br>

9. Jika tidak ada kesalahan dalam kode program, silakan klik: ``` Upload ```.

<br><br>

## Pengaturan Processing
1. Buka ``` Processing ``` terlebih dahulu, kemudian buka proyek Radar GUI dengan cara klik: ``` File ``` -> ``` Open ``` -> ``` radar_gui.pde ```.<br>

2. Sesuaikan ``` port ``` Anda dengan yang ada di ``` Arduino IDE ```. Hal ini dilakukan agar board dapat dikenali oleh ``` Processing ```, sehingga kode dapat dijalankan dengan benar.<br>

3. Langkah terakhir, silakan klik: ``` Run ```.

<br><br>

## Pengaturan MQTT Explorer
1. Buka ``` MQTT Explorer ```. Kemudian, klik Connections: ``` test.mosquitto.org ```.<br>

2. Klik ``` ADVANCED ``` -> ``` Delete All Topics ```.<br>

3. Buat ``` Topik baru ``` dengan QoS "0":
   ```
   coursera/uci/radar
   ```

4. Salin dan tempelkan ``` ID Klien ``` ke dalam proyek ``` Arduino IDE ```.<br>

5. Kemudian, klik: ``` BACK ```. Langkah terakhir, silakan klik: ``` CONNECT ```.

<br><br>

## Memulai
1. Unduh dan ekstrak repositori ini.<br>

2. Pastikan anda memiliki komponen elektronik yang diperlukan.<br>
   
3. Pastikan komponen anda telah dirancang sesuai dengan diagram.<br>
   
4. Silakan siapkan layanan ``` topik MQTT ``` pada broker.<br>
    
5. Jika Anda tidak menerapkan poin 2 dan 3 untuk tujuan pengembangan proyek, tidak masalah, tetapi perlu diketahui bahwa beberapa hal perlu diubah sesuai dengan kebutuhan Anda agar sistem dapat bekerja dengan baik.<br>

6. Pastikan semua Things telah dibuat.<br>

7. Selamat menikmati [Selesai].

<br><br>

## Sorotan
<table>
<tr>
<th width="840" colspan="2">Tampilan Perangkat Keras</th>
</tr>
<tr>
<td width="420"><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/d031c2ea-2737-4537-8948-1cac52725464" alt="IMG-1"></td>
<td width="420"><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/dd84d910-2cb5-4e75-99cd-1c362e8c7475" alt="IMG-2"></td>
</tr>
</table>
<table>
<tr>
<th width="840" colspan="2">MQTT Explorer (Data JSON pada Topik)</th>
</tr>
<tr>
<td width="420"><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/37031059-3957-40a9-a5d2-7e38a6d59037" alt="IMG-3"></td>
<td width="420"><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/fd90dd5e-9056-4480-8bf9-2177f8778d1f" alt="IMG-4"></td>
</tr>
</table>
<table>
<tr>
<th width="840" colspan="2">Serial Monitor (Publish & Subscribe)</th>
</tr>
<tr>
<td width="420"><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/54902d4c-9631-4c8b-aeb0-248be38e0456" alt="IMG-5"></td>
<td width="420"><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/5a154c46-4529-4fa8-a581-dcfdfbf04676" alt="IMG-6"></td>
</tr>
</table>
<table>
<tr>
<th width="840">Processing (Antarmuka Pengguna Grafis Radar)</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/6ee9c1eb-2d88-45ba-96fe-12c81b01bc61" alt="IMG-7"></td>
</tr>
</table>

<br><br>

## Pengingat
1. Sebelum memulai proyek, Anda harus menguji komponen terlebih dahulu untuk memastikan perangkat yang digunakan dapat bekerja dengan baik. Hal ini sudah disediakan oleh pembuat program, silakan unduh dan coba satu per satu bagian.
   
2. Penggunaan komunikasi serial antara Arduino IDE dan Processing tidak dapat dijalankan secara bersamaan, sehingga jika Anda ingin membuka Processing GUI maka pada saat yang sama Anda tidak dapat membuka Serial Monitor Arduino IDE. Hal ini juga berlaku untuk sebaliknya.

<br><br>

## Pengujian Komponen
Anda dapat mengunduh berkas uji komponen melalui tautan berikut: <a href="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/tree/master/Assets/Component%20Testing">Klik Disini</a>

<br><br>

## Penafian
Aplikasi ini dibuat dengan menyertakan sumber-sumber dari pihak ketiga. Pihak ketiga di sini adalah penyedia layanan, yang layanannya berupa pustaka, kerangka kerja, dan lain-lain. Saya ucapkan terima kasih banyak atas layanannya. Telah terbukti sangat membantu dan dapat diimplementasikan.

<br><br>

## LISENSI
LISENSI MIT - Hak Cipta (c) 2023 - Devan C. M. Wijaya, S.Kom

Dengan ini diberikan izin tanpa biaya kepada siapa pun yang mendapatkan salinan perangkat lunak ini dan file dokumentasi terkait perangkat lunak untuk menggunakannya tanpa batasan, termasuk namun tidak terbatas pada hak untuk menggunakan, menyalin, memodifikasi, menggabungkan, mempublikasikan, mendistribusikan, mensublisensikan, dan/atau menjual salinan Perangkat Lunak ini, dan mengizinkan orang yang menerima Perangkat Lunak ini untuk dilengkapi dengan persyaratan berikut:

Pemberitahuan hak cipta di atas dan pemberitahuan izin ini harus menyertai semua salinan atau bagian penting dari Perangkat Lunak.

DALAM HAL APAPUN, PENULIS ATAU PEMEGANG HAK CIPTA DI SINI TETAP MEMILIKI HAK KEPEMILIKAN PENUH. PERANGKAT LUNAK INI DISEDIAKAN SEBAGAIMANA ADANYA, TANPA JAMINAN APAPUN, BAIK TERSURAT MAUPUN TERSIRAT, OLEH KARENA ITU JIKA TERJADI KERUSAKAN, KEHILANGAN, ATAU LAINNYA YANG TIMBUL DARI PENGGUNAAN ATAU URUSAN LAIN DALAM PERANGKAT LUNAK INI, PENULIS ATAU PEMEGANG HAK CIPTA TIDAK BERTANGGUNG JAWAB, KARENA PENGGUNAAN PERANGKAT LUNAK INI TIDAK DIPAKSAKAN SAMA SEKALI, SEHINGGA RISIKO ADALAH MILIK ANDA SENDIRI.
