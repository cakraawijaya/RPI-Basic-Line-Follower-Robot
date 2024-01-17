[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Smart-Green-House-Berbasis-IoT-Mobile-Apps)
![Project](https://img.shields.io/badge/Project-Raspberry%20Pi%20Pico-light.svg?style=flat&logo=raspberrypi&logoColor=white&color=%23F7DF1E)

# Raspberry-Pi-Pico-based-Line-Follower-Robot
<strong>Proyek Tunggal Robot Pengikut Garis Berbasis Raspberry Pi Pico</strong><br><br>
Proyek ini membahas tentang bagaimana robot dapat bergerak mengikuti garis secara otomatis. Robot ini telah dilengkapi dengan sensor infrared yang bertipe ``` TCRT5000 ```. Dalam prosesnya, sensor ini bekerja berdasarkan prinsip pemantulan cahaya untuk menentukan nilai keluarannya. Jika pantulan cahaya pada objek berwarna gelap atau hitam itu dinilai kurang atau tidak ada, maka phototransistor akan berada dalam kondisi ``` OFF ``` dan modul akan memberikan keluaran ``` HIGH ```, dalam hal ini indikator led tidak akan menyala. Jika pantulan cahaya pada permukaan terang atau putih itu dinilai memadai, maka phototransistor akan berada dalam kondisi ``` ON ``` dan modul akan memberikan keluaran ``` LOW ```, dalam hal ini indikator led akan menyala.

<br><br>

## Kebutuhan Proyek
| Media | Deskripsi |
| --- | --- |
| Papan Pengembangan | Raspberry Pi Pico |
| Editor Kode | Thonny IDE |
| Bootloader | MicroPython UF2 |
| Bahasa Pemrograman | MicroPython |
| Paket | machine & utime |
| Aktuator | Gear Motor / Motor DC (x2) |
| Sensor | KR08200: Sensor IR Pelacakan Garis 3 Arah, Merek: Funduino (x1) |
| Saklar | KCD11: Saklar Pengayun SPST (x1) |
| Komponen Lainnya | Kabel mikro usb (x1), Kabel jumper, Baterai Li-ion 18650 (x2), Tempat baterai seri 2 slot (x1), Roda robot (x2), Roda kastor (x1), Motor driver L298N (x1), Kerangka robot mobil (x1), DLL |

<br><br>

## Unduh & Instal
1. Thonny IDE

   ```
   https://thonny.org/
   ```
<br>

2. MicroPython UF2

   ```
   https://bit.ly/MicroPython_UF2
   ```
   
<br><br>

## Rancangan Proyek
<table>
<tr>
<th width="420">Diagram Blok</th>
<th width="420">Diagram Ilustrasi</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/Raspberry-Pi-Pico-based-Line-Follower-Robot/assets/54527592/2d13dd05-7f81-45cb-9e72-9e8d3ff9a8ef" alt="Block-Diagram"></td>
<td><img src="https://github.com/devancakra/Raspberry-Pi-Pico-based-Line-Follower-Robot/assets/54527592/7b26b147-abfd-4fa1-9c89-d84fc8ea3f2c" alt="Pictorial-Diagram"></td>
</tr>
</table>
<table>
<tr>
<th width="840">Pengkabelan</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/Raspberry-Pi-Pico-based-Line-Follower-Robot/assets/54527592/96c6e986-01fb-4b7c-bd00-55ee90bf30d6" alt="Wiring"></td>
</tr>
</table>

<br><br>

## Pengaturan Bootloader MicroPython
1. ``` Unggah firmware ``` :

   • Tekan dan tahan tombol ``` BOOTSEL ``` yang ada di papan Raspberry Pi Pico sembari menyambungkan ke komputer melalui kabel mikro USB.

   • Setelah Raspberry Pi Pico dikenali oleh komputer (terhubung), maka segera lepaskan tombol ``` BOOTSEL ```.
   
   • Ketika berhasil terhubung, maka sebuah drive baru bernama ``` RPI-RP2 ``` akan terbuka.
   
   • ``` Seret -> Lepaskan ``` atau ``` Salin -> Tempelkan ``` file firmware ``` MicroPython UF2 ``` ke dalam drive ``` RPI-RP2 ```.<br><br>

2. Setelah prosesnya berhasil, maka drive ``` RPI-RP2 ``` akan otomatis tertutup.

<br><br>

## Pengaturan Thonny IDE
1. Buka ``` Thonny IDE ``` terlebih dahulu.<br><br>

2. Klik ``` Tools ``` -> lalu pilih ``` Options... ``` -> selanjutnya pilih :<br><br>
   
   • ``` Menu Interpreter ```, kemudian ubah bagian :

      - ``` Interpreter ``` -> ``` MicroPython (Raspberry Pi Pico) ```
        
      - ``` Port ``` -> ``` Board CDC @ COM... ```
  
      - ``` Restart interpreter before running a script ``` -> ``` hapus centang ```<br><br>
   
   • ``` Menu Editor ```, kemudian centang semua opsinya kecuali: ``` Indent with tab characters ```.<br><br>

3. Jika tampilan berkas belum ada di Thonny IDE, maka silakan anda klik bagian ``` View ``` -> lalu pilih ``` Files ``` untuk menampilkannya.<br><br>

4. Kemudian cari berkas yang bernama ``` rpipico_line_follower.py ``` di komputer Anda -> lalu ubah nama berkasnya menjadi: ``` main.py ``` agar nantinya dapat dikenali oleh Raspberry Pi Pico saat mau dioperasikan.<br><br>
   
5. Klik kanan pada berkas tersebut -> pilih ``` Upload to / ```.<br><br>

6. Buka berkas ``` rpipico_line_follower.py ``` yang ada di penyimpanan ``` Raspberry Pi Pico ``` -> lalu klik ``` Run current script (F5) ```.<br><br>

7. Kode program berhasil di eksekusi -> tandanya: ``` %run -c $EDITOR_CONTENT ```.

<br><br>

## Memulai
1. Unduh dan ekstrak repositori ini.<br><br>
   
2. Pastikan anda memiliki komponen elektronik yang diperlukan.<br><br>
   
3. Pastikan komponen anda telah dirancang sesuai dengan diagram.<br><br>
    
4. Konfigurasikan perangkat anda menurut pengaturan di atas.<br><br>

5. Selamat menikmati [Selesai].

<br><br>

## Sorotan
<img src="https://github.com/devancakra/Raspberry-Pi-Pico-based-Line-Follower-Robot/assets/54527592/684c7c48-d779-46ba-8813-821667959d09" alt="robot-line-follower">

<br><br>

## LISENSI
LISENSI MIT - Hak Cipta (c) 2023 - Devan C. M. Wijaya, S.Kom

Dengan ini diberikan izin tanpa biaya kepada siapa pun yang mendapatkan salinan perangkat lunak ini dan file dokumentasi terkait perangkat lunak untuk menggunakannya tanpa batasan, termasuk namun tidak terbatas pada hak untuk menggunakan, menyalin, memodifikasi, menggabungkan, mempublikasikan, mendistribusikan, mensublisensikan, dan/atau menjual salinan Perangkat Lunak ini, dan mengizinkan orang yang menerima Perangkat Lunak ini untuk dilengkapi dengan persyaratan berikut:

Pemberitahuan hak cipta di atas dan pemberitahuan izin ini harus menyertai semua salinan atau bagian penting dari Perangkat Lunak.

DALAM HAL APAPUN, PENULIS ATAU PEMEGANG HAK CIPTA DI SINI TETAP MEMILIKI HAK KEPEMILIKAN PENUH. PERANGKAT LUNAK INI DISEDIAKAN SEBAGAIMANA ADANYA, TANPA JAMINAN APAPUN, BAIK TERSURAT MAUPUN TERSIRAT, OLEH KARENA ITU JIKA TERJADI KERUSAKAN, KEHILANGAN, ATAU LAINNYA YANG TIMBUL DARI PENGGUNAAN ATAU URUSAN LAIN DALAM PERANGKAT LUNAK INI, PENULIS ATAU PEMEGANG HAK CIPTA TIDAK BERTANGGUNG JAWAB, KARENA PENGGUNAAN PERANGKAT LUNAK INI TIDAK DIPAKSAKAN SAMA SEKALI, SEHINGGA RISIKO ADALAH MILIK ANDA SENDIRI.
