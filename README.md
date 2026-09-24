# PHP-practical-program-1

<!DOCTYPE html>
<html>
<head>
    <title>Calculator</title>
    <style>
        body { text-align:center; font-family:Arial; }
        input, select { padding:8px; margin:5px; }
    </style>
</head>
<body>

<h2>Simple Calculator</h2>

<form method="post">
    <input type="number" name="a" placeholder="First Number" required>
    <input type="number" name="b" placeholder="Second Number" required>

    <select name="op">
        <option value="+">+</option>
        <option value="-">-</option>
        <option value="*">*</option>
        <option value="/">/</option>
    </select>

    <input type="submit" name="cal" value="Calculate">
</form>

<?php
if(isset($_POST['cal']))
{
    $a = $_POST['a'];
    $b = $_POST['b'];
    
    switch($_POST['op'])
    {
        case "+": $r = $a + $b; break;
        case "-": $r = $a - $b; break;
        case "*": $r = $a * $b; break;
        case "/": $r = $a / $b; break;
    }

    echo "<h3>Result = $r</h3>";
}
?>

</body>
</html>


Output
        
First Number:  10
Second Number: 5
Operation:     +  -  *  /

Result = 15


For different operations:

10 + 5 = 15
10 - 5 = 5
10 * 5 = 50
10 / 5 = 2
