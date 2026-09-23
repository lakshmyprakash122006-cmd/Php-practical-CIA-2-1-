# Php-practical-CIA-2-1-
Program 
<html>
<body>

<h2>Electricity Bill Calculator</h2>

<form method="post">

Enter Units:
<input type="number" name="units"><br><br>

<input type="submit" name="submit" value="Calculate">

</form>

<?php

function calculateBill($units)
{
    if($units <= 100)
    {
        $bill = $units * 1;
    }
    elseif($units <= 200)
    {
        $bill = $units * 2;
    }
    else
    {
        $bill = $units * 3;
    }

    return $bill;
}

if(isset($_POST['submit']))
{
    $units = $_POST['units'];

    $bill = calculateBill($units);

    echo "Units: $units<br>";
    echo "Electricity Bill: Rs. $bill";
}

?>

</body>
</html>

Output:Units: 500
Electricity bill: 2000
