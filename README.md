### Program sederhana input data karyawan menggunakan php

kali ini kita akan membuat sebuah porgram sederhana yaitu input data karyawan menggunakan bahasa pemrogramman PHP

> Tools yang dibutuhkan.
- XAMPP
- Visual Studio Code
- Browser (google chrome)

Pertama buat lah folder di dalam htdocs dengan nama **Lab2Web** lalu buat file bernama **index.php**
untuk penamaan folder dan file kalian bebas menamakannya.
Setelah itu buka folder tersebut dengan Visual Studio Code seperti gambar dibawah ini

![gambar]![image](https://github.com/ririn27/TUGAS-WEB2-KE-1/assets/115934294/5ceff842-2fa7-4d0e-92e3-986ffad81345)


selanjutnya buka file **index.php** lalu ikuti kode seperti gambar dibawah :

![kode1](![image](https://github.com/ririn27/TUGAS-WEB2-KE-1/assets/115934294/9e88016d-d53f-47eb-aba7-2cc9a75fdfde)
)
> Pembahasan
Pada kode diatas merupakan kode php dalam menangani formulir yang akan diinput,

`
if (isset($_POST['submit'])) {
`
ini pengecekan jika ada  post submit yang dikirim maka lakukan perintah berikut, jika tidak ada dia keluar blok kurang kurawal buka / tutup

Pada bagian berikut dilakukan pengecekan mengenai pekerjaan, jika pekerjaannya sebagai  **Software Engineer** maka gaji nya 23000000 dan seterusnya tergantung pada yang diinputkan nanti didalam formulir

```
$pekerjaan = $_POST["pekerjaan"];
  if ($pekerjaan == "Software Engineer") {
    $gaji = 23000000;
  } else if ($pekerjaan == "Data Analyst") {
    $gaji = 25000000;
  } else if ($pekerjaan == "Design Graphic") {
    $gaji = 19000000;
  } else if ($pekerjaan == "Network Engineer") {
    $gaji = 22000000;
  } else if ($pekerjaan == "QA Engineer") {
    $gaji = 18000000;
  } else if ($pekerjaan == "DevOps Engineer") {
    $gaji = 23500000;
  } else {
    $gaji = 0;
  }
```

Selanjutnya pada bagian blok kode berikut merupakan perhitungan umur berdasarkan tanggal lahir yang diinputkan, kita menggunakan fungsi bawaan php yaitu `DateTime()` yang mana nanti kita dapat mengetahui umur yang akan diinputkan berdasarkan tanggal lahirnya. lalu kita simpan di variabel umur.

```
$tanggal_lahir = new DateTime($_POST['tanggal_lahir']);

  $hari_ini = new DateTime('today');
  $tahun = $tanggal_lahir->diff($hari_ini)->y;
  $bulan = $tanggal_lahir->diff($hari_ini)->m;
  $hari = $tanggal_lahir->diff($hari_ini)->d;

  $umur = $tahun . " tahun " . $bulan . " bulan " . $hari . " hari ";

```

lanjut ke kode berikut :

kode berikut merupakan kerangka html yang akan menampilkan formulir dan data yang diinputkan, pada kode ini kita menambahkan style css agar terlihat menarik.

![kode2]![image](https://github.com/ririn27/TUGAS-WEB2-KE-1/assets/115934294/0063e139-d293-4987-a49a-f4c9890c1e29)


![kode3]![image](https://github.com/ririn27/TUGAS-WEB2-KE-1/assets/115934294/5c8ebcea-ad8b-41d6-bad0-d0fd38a1d5a7)


Selanjutnya tambahkan kode berikut :

pada kode dibawah ini merupakan tag formulir html. sebagai formulir dan hasil dari inputan yang akan diinputkan nanti.

![kode4]![image](https://github.com/ririn27/TUGAS-WEB2-KE-1/assets/115934294/56450e99-aa23-4d5c-ae99-1449597f7e87)


setelah selesai saatnya kita jalankan programnya dengan cara buka xampp control panel lalu start apache, jika sudah buka browser lalu ketikan **`localhost/Lab2Web`**


Berikut hasil program yang akan muncul sebelum diinput dan sesudah diinput :


![hasi2]![WhatsApp Image 2024-03-19 at 23 22 22_2c501090](https://github.com/ririn27/TUGAS-WEB2-KE-1/assets/115934294/098bd291-36f4-49ba-9cb4-f14d5b96d005)


Selesai terima kasih semoga bermanfaat.

