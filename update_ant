<?php
$servername = "localhost";
$username = "seu_usuario";
$password = "sua_senha";
$dbname = "aquavibes";

$conn = new mysqli($servername, $username, $password, $dbname);

$device = $_POST['device'];
$temp = $_POST['temp'];
$ph = $_POST['ph'];
$turbidez = $_POST['turbidez'];
$nivel = $_POST['nivel'];
$aux = $_POST['aux'];
$ilum = $_POST['ilum'];

$sql = "INSERT INTO dados (device, temperatura, ph, turbidez, nivel_minimo, aux, ilum, timestamp) 
        VALUES ('$device', $temp, $ph, $turbidez, $nivel, $aux, $ilum, NOW())
        ON DUPLICATE KEY UPDATE 
        temperatura = $temp, ph = $ph, turbidez = $turbidez, nivel_minimo = $nivel, 
        aux = $aux, ilum = $ilum, timestamp = NOW()";

$conn->query($sql);
$conn->close();
echo "OK";
?>
