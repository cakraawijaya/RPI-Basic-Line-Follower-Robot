[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/cakraawijaya/RPI-Basic-Line-Follower-Robot?logo=Codeforces&logoColor=white&color=%23F7DF1E)
![Project](https://img.shields.io/badge/Project-Raspberry-light.svg?style=flat&logo=raspberrypi&logoColor=white&color=%23F7DF1E)
![Type](https://img.shields.io/badge/Type-Personal%20Experiment-light.svg?style=flat&logo=gitbook&logoColor=white&color=%23F7DF1E)

# RPI-Basic-Line-Follower-Robot
Robot adalah alat yang mampu meringankan beban manusia. Robot dapat dikendalikan oleh manusia secara langsung, namun sebenarnya robot juga dapat mengambil keputusannya sendiri jika diberi algoritma cerdas. Jenis robot yang sering dipakai dalam kegiatan sekolah yaitu robot beroda. Robot beroda adalah robot yang bergerak dengan menggunakan roda. Tujuan diadakannya proyek ini adalah untuk mendapatkan kemampuan robot yang dapat mengenali garis. Proyek ini telah dilaksanakan dan memakan waktu kurang lebih 3 hari. Robot ini telah dilengkapi dengan sensor infrared yang bertipe ``` TCRT5000 ```. Dalam prosesnya, sensor ini bekerja berdasarkan prinsip pemantulan cahaya yang didapatkan dari objek yang kemudian diteruskan ke fototransistor untuk ditentukan nilai keluarannya. Jika pantulan cahaya pada objek berwarna gelap atau hitam itu dinilai kurang memadai, maka modul sensor akan memberikan keluaran ``` LOW ```, dalam hal ini indikator led tidak akan menyala. Jika pantulan cahaya pada permukaan terang atau putih itu dinilai memadai, maka modul sensor akan memberikan keluaran ``` HIGH ```, dalam hal ini indikator led akan menyala. Manfaat dari pembuatan proyek ini tidak lain adalah untuk menambah wawasan. Hasil penelitian menunjukkan bahwa sistem yang dibuat dapat berfungsi dengan baik.

<br><br>

## Kebutuhan Proyek
| Bagian | Deskripsi |
| --- | --- |
| Papan Pengembangan | Raspberry Pi Pico |
| Editor Kode | Thonny IDE |
| Bootloader | MicroPython UF2 |
| Bahasa Pemrograman | MicroPython |
| Paket | • machine (bawaan)<br>• utime (bawaan) |
| Aktuator | Gear Motor / Motor DC (x2) |
| Sensor | KR08200: Sensor IR Pelacakan Garis 3 Arah - Merek: Funduino (x1) |
| Komponen Lainnya | • Kabel USB Mikro - USB tipe A (x1)<br>• Kabel USB Mikro - JST 2 pin (x1)<br>• Kabel jumper (1 set)<br>• Baterai Li-ion 18650 (x2)<br>• Tempat baterai seri 2 slot (x1)<br>• Roda robot (x2)<br>• Roda kastor (x1)<br>• Motor driver L298N (x1)<br>• Kerangka robot mobil (x1)<br>• Baut spicer (1 set)<br>• Baut plus (1 set)<br>• Mur (1 set) |

<br><br>

## Unduh & Instal
1. Thonny IDE

   <table><tr><td width="810">

   ```
   https://bit.ly/ThonnyIDE_Installer
   ```

   </td></tr></table><br>

2. MicroPython UF2

   <table><tr><td width="810">

   ```
   https://bit.ly/MicroPython_UF2_RPIpico
   ```

   </td></tr></table>
   
<br><br>

## Rancangan Proyek
<table>
<tr>
<th width="420">Diagram Blok</th>
<th width="420">Diagram Ilustrasi</th>
</tr>
<tr>
<td><img src="Assets/Documentation/Diagram/Block Diagram.jpg" alt="block-diagram"></td>
<td><img src="Assets/Documentation/Diagram/Pictorial Diagram.jpg" alt="pictorial-diagram"></td>
</tr>
</table>
<table>
<tr>
<th width="840">Pengkabelan</th>
</tr>
<tr>
<td><img src="Assets/Documentation/Table/Device Wiring.jpg" alt="wiring"></td>
</tr>
</table>

<br><br>

## Pengaturan Bootloader MicroPython
1. ``` Unggah firmware ``` :

   <table><tr><td width="810">    

      - Tekan dan tahan tombol ``` BOOTSEL ``` yang ada di papan ``` Raspberry Pi Pico ``` sembari menyambungkan ke komputer melalui kabel ``` mikro USB ```.
        
      - Setelah ``` Raspberry Pi Pico ``` dikenali oleh komputer (terhubung), maka segera lepaskan tombol ``` BOOTSEL ```.
      
      - Ketika berhasil terhubung, maka sebuah drive baru bernama ``` RPI-RP2 ``` akan terbuka.
      
      - ``` Seret -> Lepaskan ``` atau ``` Salin -> Tempelkan ``` file firmware ``` MicroPython UF2 ``` ke dalam drive ``` RPI-RP2 ```.

   </td></tr></table><br>

2. Setelah prosesnya berhasil, maka drive ``` RPI-RP2 ``` akan otomatis tertutup.<br><br>

3. Secara umum, unggah firmware itu hanya perlu dilakukan sekali saja saat anda pertama kali menggunakan board ``` Raspberry Pi Pico ```.

<br><br>

## Pengaturan Thonny IDE
1. Buka ``` Thonny IDE ``` terlebih dahulu.<br><br>

2. Klik ``` Tools ``` -> lalu pilih ``` Options... ``` -> selanjutnya pilih :<br><br>
   
   • ``` Menu Interpreter ```, kemudian ubah bagian :

      <table><tr><td width="810">

      - ``` Interpreter ``` -> ``` MicroPython (Raspberry Pi Pico) ```
        
      - ``` Port ``` -> ``` Board CDC @ COM... ```
  
      - ``` Restart interpreter before running a script ``` -> ``` hapus centang ```

   </td></tr></table>
   
   • ``` Menu Editor ```, kemudian centang semua opsinya kecuali: ``` Indent with tab characters ```.<br><br>

3. Jika tampilan berkas belum ada di ``` Thonny IDE ```, maka silakan anda klik bagian ``` View ``` -> lalu pilih ``` Files ``` untuk menampilkannya.<br><br>

4. Kemudian cari berkas bernama ``` main.py ``` di dalam direktori: ``` Raspberry-Pi-Pico-based-Line-Follower-Robot/Src ```.<br><br>
   
5. Klik kanan pada berkas tersebut -> pilih ``` Upload to / ```.<br><br>

6. Buka berkas ``` main.py ``` yang ada di penyimpanan ``` Raspberry Pi Pico ``` -> lalu klik ``` Run current script (F5) ```.<br><br>

7. Kode program berhasil di eksekusi -> tandanya: ``` %run -c $EDITOR_CONTENT ```.<br><br>

8. Jika saat unggah program masih terdapat masalah, maka coba periksa pada bagian ``` interpreter ``` / ``` port ``` / ``` yang lainnya ```.

<br><br>

## Memulai
1. Unduh dan ekstrak repositori ini.<br><br>
   
2. Pastikan anda memiliki komponen elektronik yang diperlukan.<br><br>
   
3. Pastikan komponen anda telah dirancang sesuai dengan diagram.<br><br>
    
4. Konfigurasikan perangkat anda menurut pengaturan di atas.<br><br>

5. Selamat menikmati [Selesai].

<br><br>

## Sorotan
<img width="840" src="Assets/Documentation/Experiment/Device.jpg" alt="robot-line-follower">

<br><br>

## <img src="https://github.com/user-attachments/assets/932b96eb-cbc7-42f1-8938-43cb431889a5" width="16" height="16"> Catatan
<blockquote>
   Hasil pengujian menunjukkan bahwa pergerakan motor masih belum cukup mulus. Di masa mendatang, akan lebih baik jika menggunakan algoritma cerdas seperti PID untuk meningkatkan presisi dan stabilitas pergerakan motor.
</blockquote>

<br><br>

## Apresiasi
Jika karya ini bermanfaat bagi anda, maka dukunglah karya ini sebagai bentuk apresiasi kepada penulis dengan mengklik tombol ``` ⭐Bintang ``` di bagian atas repositori.

<br><br>

## LISENSI
LISENSI MIT - Hak Cipta © 2023 - Devan C. M. Wijaya, S.Kom

Dengan ini diberikan izin tanpa biaya kepada siapa pun yang mendapatkan salinan perangkat lunak ini dan file dokumentasi terkait perangkat lunak untuk menggunakannya tanpa batasan, termasuk namun tidak terbatas pada hak untuk menggunakan, menyalin, memodifikasi, menggabungkan, mempublikasikan, mendistribusikan, mensublisensikan, dan/atau menjual salinan Perangkat Lunak ini, dan mengizinkan orang yang menerima Perangkat Lunak ini untuk dilengkapi dengan persyaratan berikut:

Pemberitahuan hak cipta di atas dan pemberitahuan izin ini harus menyertai semua salinan atau bagian penting dari Perangkat Lunak.

DALAM HAL APAPUN, PENULIS ATAU PEMEGANG HAK CIPTA DI SINI TETAP MEMILIKI HAK KEPEMILIKAN PENUH. PERANGKAT LUNAK INI DISEDIAKAN SEBAGAIMANA ADANYA, TANPA JAMINAN APAPUN, BAIK TERSURAT MAUPUN TERSIRAT, OLEH KARENA ITU JIKA TERJADI KERUSAKAN, KEHILANGAN, ATAU LAINNYA YANG TIMBUL DARI PENGGUNAAN ATAU URUSAN LAIN DALAM PERANGKAT LUNAK INI, PENULIS ATAU PEMEGANG HAK CIPTA TIDAK BERTANGGUNG JAWAB, KARENA PENGGUNAAN PERANGKAT LUNAK INI TIDAK DIPAKSAKAN SAMA SEKALI, SEHINGGA RISIKO ADALAH MILIK ANDA SENDIRI.
