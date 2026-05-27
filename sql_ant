CREATE DATABASE aquavibes;
USE aquavibes;

CREATE TABLE dados (
    device VARCHAR(50) PRIMARY KEY,
    temperatura FLOAT,
    ph FLOAT,
    turbidez FLOAT,
    nivel_minimo INT,
    aux INT,
    ilum INT,
    timestamp DATETIME
);

CREATE TABLE comandos (
    device VARCHAR(50) PRIMARY KEY,
    comando_manual INT DEFAULT 0,
    aux INT DEFAULT 0,
    ilum INT DEFAULT 0
);
