# Tugas-1-Pemrograman-Web
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kalkulator</title>
</head>
<body>
    <h1>Kalkulator Sederhana</h1>
    <form>
   
        <input type="number" name="a" placeholder="Bilangan a">

        <select name="operator">
            <option selected dosabled>Pilih Operator</option>
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="*">*</option>
            <option value="/">/</option>
</select>

<input type="number" name="b" placeholder="Bilangan b">
<button  type="button" onclick="location.href = '?clear' ">Clear</button>
<button type="submit">Hitung</button>

</form>

</body>
</html>


<?php
    if ($_POST): 
   $a = (double) $_POST['a'];
   $b = (double) $_POST['b'];
   $operator = $_POST['operator'];

   switch ($operator){
    case '+':
        $hasil = $a + $b;
        break;
        case '-':
            $hasil = $a - $b;
            break;
            case '*':
                $hasil = $a * $b;
                break;
                case '/':
                    $hasil = $a / $b;
                    break;
                }
    ?>
