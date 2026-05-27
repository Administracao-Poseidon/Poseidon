<?php
$device = $_GET['device'];
$conn = new mysqli("localhost", "usuario", "senha", "aquavibes");

$sql = "SELECT comando_manual, aux, ilum FROM comandos WHERE device = '$device'";
$result = $conn->query($sql);
$row = $result->fetch_assoc();

echo json_encode([
    'alimentador_manual' => $row['comando_manual'] ?? 0,
    'aux' => $row['aux'] ?? 0,
    'ilum' => $row['ilum'] ?? 0
]);

// Resetar comandos após leitura
$conn->query("UPDATE comandos SET comando_manual = 0 WHERE device = '$device'");
$conn->close();
?>
