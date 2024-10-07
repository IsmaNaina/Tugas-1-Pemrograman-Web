# Tugas-1-Pemrograman-Web
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kalkulator</title>
</head>
<body>
    <h1>Aplikasi Kalkulator Sederhana</h1>
    <form method="POST">
       Masukkan Bilangan Pertama <input type="number" name="nilai1" placeholder="Angka Pertama" required> <br>
        <select name="operator" required>
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="*">*</option>
            <option value="/">/</option>
        </select><br>
        Masukkan Bilangan Kedua  <input type="number" name="nilai2" placeholder="Angka Kedua" required> <br>
        <button type="submit">Hitung</button>
    </form>
    <?php
    if ($_SERVER["REQUEST_METHOD"] == "POST") {
        $nilai1 = $_POST['nilai1'];
        $nilai2 = $_POST['nilai2'];
        $operator = $_POST['operator'];
        $hasil = 0;

        switch ($operator) {
            case '+':
                $hasil = $nilai1 + $nilai2;
                break;
            case '-':
                $hasil = $nilai1 - $nilai2;
                break;
            case '*':
                $hasil = $nilai1 * $nilai2;
                break;
                case '/':
                    if ($nilai1 != 0) {
                        $hasil = $nilai1 / $nilai2;
                    } else {
                        echo "Error: Pembagian dengan nol!";
                    }
                    break;
            }
    
            if ($operator != '/') {
                echo "<h2>Hasil Perhitungan: $hasil</h2>";
            }
        }
        ?>
    </body>
    </html>
  
