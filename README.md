<!DOCTYPE html>
<html lang="es">
<head>
 <meta charset="UTF-8">
 <title>Formulario de Registro de Hoteles</title>
 <script>
 function validarFormulario() {
 var nombre = document.getElementById('nombre').value.trim();
 var ubicacion = document.getElementById('ubicacion').value.trim();
 var habitaciones = document.getElementById('habitaciones').value.trim();
 var tarifa = document.getElementById('tarifa').value.trim();
 if (nombre === '' || ubicacion === '' || habitaciones === '' || tarifa === '') {
 alert('Todos los campos son obligatorios');
 return false;
 }
 if (isNaN(habitaciones) || isNaN(tarifa)) {
 alert('Las habitaciones disponibles y la tarifa deben ser números');
 return false;
 }
 return true;
 }
 </script>
</head>
<body>
 <h2>Registro de Hoteles</h2>
 <form action="insertar_hotel.php" method="post" onsubmit="return validarFormulario()">
 <label for="nombre">Nombre:</label><br>
 <input type="text" id="nombre" name="nombre"><br>

 <label for="ubicacion">Ubicación:</label><br>
 <input type="text" id="ubicacion" name="ubicacion"><br>

 <label for="habitaciones">Habitaciones Disponibles:</label><br>
 <input type="number" id="habitaciones" name="habitaciones"><br>

 <label for="tarifa">Tarifa por Noche:</label><br>
 <input type="number" id="tarifa" name="tarifa" step="0.01"><br><br>

 <input type="submit" value="Registrar Hotel">
 </form>
</body>
</html>
