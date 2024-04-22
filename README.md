// Importa el módulo express
const express = require('express');

// Crea una instancia de la aplicación Express
const app = express();

// Define el método GET en la ruta '/info'
app.get('/info', (req, res) => {
    // Crea un objeto con los campos especificados
    const response = {
        Nombre: "Juan Pérez",
        Documento: 123456789,
        Correo: "juan.perez@example.com",
        Teléfono: 987654321,
        Dirección: "Calle Principal 123",
        Valor: 1000,
        Concepto: "Compra de productos"
    };

    // Envía el objeto como respuesta en formato JSON
    res.json(response);
});

// Especifica el puerto en el que escuchará la aplicación
const port = 3000;

// Inicia el servidor en el puerto especificado
app.listen(port, () => {
    console.log(`Servidor iniciado en http://localhost:${port}`);
});

