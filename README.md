|  Muhammad Bisma  |    312010443    |
|------------------|-----------------|
|  TI.21.A.1       | Pemrograman Web |

## Pertemuan 9 Lab7Web
Dalam pertemuan ini kita akan mempelajari PHP Dasar dengan beberapa program code PHP nya.

# PHP Dasar

## 1). Instal XAMPP
![install](img/1.png)
Install XAMPP kemudian ekstrak file dan sesuaikan lokasi penyimpanannya.

## 2). Menjalankan XAMPP
![start](img/2.png)
Menjalankan XAMPP dengan cara klik tombol Start pada server Apache seperti di gambar.

## 3). Memulai PHP 
![php](img/3.png)
Buat folder lab7_php_dasar pada root directory web server (c:xampp/htdocs)

Kemudian akses directory pada web server dengan mengakses URL : http://localhost/Lab7Web/lab7_php_dasar/
![hasil](img/4.png)

## 4). PHP Dasar
![dasar](img/5.png) 
Berikut hasil run PHP Dasar
### Contoh Coding
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHP Dasar</title>
</head>
<body>
    <h1>Belajar PHP Dasar</h1>
    <?php
        echo "Hello World";
    ?>
```

## 5). Variabel PHP
![variabel](img/6.png)
Berikut hasil run variabel pada program di PHP

### Contoh Coding
```php
 <!-- Variabel PHP -->
    <h2>Menggunakan Variabel</h2>
    <?php
        $nim = "0411500400";
        $nama = 'Abdullah';
        echo "NIM : " . $nim . "<br>";
        echo "Nama : $nama";
    ?>
```

## 6). Predefine $_GET
![predefine](img/7.png)
Buat file baru dalam directory lab7_php_dasar dengan nama filenya adalah latihan2.php dan untuk mengaksesnya menggunakan URL : http://localhost/Lab7Web/lab7_php_dasar/latihan2.php?nama=%20Bisma

### Contoh Coding
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHP Dasar</title>
</head>
<body>
    <!-- Variabel $_GET -->
    <h2>Predefine Variabel</h2>
<?php
    echo 'Selamat Datang'. $_GET['nama'];
?>
</body>
</html>
```

## 7). Membuat Form Input
![form](img/8.png)
Buat File baru dengan nama latihan3.php dalam directory folder lab7_php_dasar 

Berikut adalah hasil atau tampilan dalam membuat form dalam php dengan variable $_POST 

### Contoh Coding
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
<h2>Form Input</h2>
<form method="post">
    <label>Nama: </label>
    <input type="text" name="nama">
    <input type="submit" value="Kirim">
</form>
<?php
    echo 'Selamat Datang ' . $_POST['nama'];
?>
</body>
</html>
```

## 8). Operator
![operator](img/9.png)
Membuat OPERATOR dalam php seperti contoh hasil tampilan di atas beserta code nya.

### Contoh Coding
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHP Dasar</title>
</head>
<body>
<?php
    $gaji = 1000000;
    $pajak = 0.1;
    $thp = $gaji - ($gaji*$pajak);
        echo "Gaji sebelum pajak = Rp. $gaji <br>";
        echo "Gaji yang dibawa pulang = Rp. $thp";
?>
</body>
</html>
```

## 9). Kondisi IF
![kondisi_if](img/10.png)
Pengondisian IF ELSE seperti hasil tampilan dan code digambar atas

### Contoh Coding
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHP Dasar</title>
</head>
<body>
    <h2>Kondisi IF</h2>
<?php
    $nama_hari = date("l");
        if ($nama_hari == "Sunday") {
            echo "Minggu";
        } elseif ($nama_hari == "Monday") {
            echo "Senin";
        } else {
            echo "Selasa";
        }
?>
</body>
</html>
```

## 10). Kondisi Switch
![kondisi_switch](img/11.png)
Contoh penggunaan pengondisian SWICTH CASE dengan Break seperti contoh hasil diatas beserta code.

### Contoh Coding
```php
 <h2>Kondisi Switch</h2>
<?php
    $nama_hari = date("l");
    switch ($nama_hari) {
        case "Sunday":
            echo "Minggu";
            break;
        case "Monday":
            echo "Senin";
            break;
        case "Tuesday":
            echo "Selasa";
            break;
        default:
            echo "Sabtu";
    }
    echo"/$nama_hari";
?>
```

## 11). Perulangan For
![perulangan_for](img/12.png)
Menggunakan PERULANGAN FOR seperti hasil dan code di atas

### Contoh Coding
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHP Dasar</title>
</head>
<body>
    <h2>Perulangan For</h2>
<?php
        echo "Perulangan 1 sampai 10 <br />";
    for ($i=1; $i<=10; $i++) {
        echo "Perulangan ke: " . $i . '<br />';
    }
        echo "Perulangan Menurun dari 10 ke 1 <br />";
    for ($i=10; $i>=1; $i--) {
        echo "Perulangan ke: " . $i . '<br />';
    }
?>
</body>
</html>
```

## 12). Perulangan While
![while](img/13.png)
Menggunakan PERULANGAN WHILE seperti hasil gambar dan code di atas.

```php
 <h2>Perulangan While</h2>
<?php
        echo "Perulangan 1 sampai 10 <br />";
        $i=1;
    while ($i<=10) {
        echo "Perulangan ke: " . $i . '<br />';
        $i++;
    }
?>
```

## 13). Perulangan Dowhile
![dowhile](img/14.png)
Menggunakan PERULANGAN DOWHILE seperti hasil gambar di atas yg beserta code php nya.

### Contoh Coding
```php
 <h2>Perulangan Dowhile</h2>
<?php
        echo "Perulangan 1 sampai 10 <br />";
        $i=1;
    do {
        echo "Perulangan ke: " . $i . '<br />';
        $i++;
        } while ($i<=10);
?>
```

# Pertanyaan & Tugas
Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan nama , tanggal lahir dan pekerjaan . Kemudian tampilkan outputnya dengan menghitung umur berdasarkan inputan tanggal lahir . Dan pilihan pekerjaan dengan gaji yang berbeda-beda sesuai pilihan pekerjaan.

![tugas](img/15.png)

### Contoh Coding
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tugas</title>
</head>
<body>
   <h2>TUGAS</h2>
    <form class="form" method="post" >
            <label>Nama: </label>
            <br>
            <input type="text" name="nama">
            <br>
            <label>Tanggal Lahir: </label>
            <br>
            <input type="text" name="tgl_lahir">
            <br>
            <label>Pekerjaan: </label>
            <br>
            <select name='pekerjaan'>
                <option value="-">>---Pilih Pekerjaan---<</option>
                <option value='Operator'>Operator</option>
                <option value='Staff Admin'>Staff Admin</option>
                <option value='HRD'>HRD</option>
                <option value='Maintenance'>Maintenance</option>
                <option value="QC">QC</option>
            </select>
            <br>
            <br>
            <button type="submit">Kirim</button>
    </form>
    <h2>HASIL</h2>

    <?php
        # Memanggil Nama
        echo 'Nama: ' . $_POST['nama'];

        # Merubah Tanggal Lahir menjadi Umur (Tahun)
        $tgl_lahir = @$_POST['tgl_lahir'];

        $lahir = new DateTime($tgl_lahir);
        $hari_ini = new DateTime();

        $diff = $hari_ini->diff($lahir);

        # Memanggil fungsi umur yg sudah dibuat diatas
        echo "<br> Umur: ". $diff->y ." Tahun";

        # Memanggil pekerjaan
        echo "<br> Pekerjaan: ". $_POST['pekerjaan'];

        # Kondisi if pekerjaan untuk menentukan gaji
        $pekerjaan = @$_POST['pekerjaan'];

        if($pekerjaan == "Operator"){
            echo '<br> Gaji: Rp. 6.000.000,-';
        }elseif($pekerjaan == "Staff Admin"){
            echo '<br> Gaji: Rp. 7.500.000,-';
        }elseif($pekerjaan == "HRD"){
            echo '<br> Gaji: Rp. 10.000.000,-';
        }elseif($pekerjaan == "Maintenance"){
            echo '<br> Gaji: Rp. 9.000.000,-';
        }elseif ($pekerjaan == "QC"){
            echo '<br> Gaji: Rp. 7.000.000,-';
        }

    ?>
  </body>
</html>
```

# TERIMA KASIH