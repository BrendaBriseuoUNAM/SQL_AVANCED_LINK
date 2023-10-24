<h2>CASE</h2>
<h3>Ejercicio 2</h3>
SELECT 
  CASE 1
  WHEN 1 THEN 'UNO'
  WHEN 2 THEN 'DOS'
  WHEN 3 THEN 'TRES'
  ELSE 'OTRO'
  END AS VALOR

<h3>Ejercicio 2</h3>
SELECT id_producto,id_fabricante,
  CASE 
  WHEN cantidad > 2 THEN 'Más de dos productos vendidos'
  WHEN cantidad = 2 THEN 'Dos productos vendidos'
  ELSE 'Menos de dos productos vendidos'
  END AS  cantidad
  from detalles;

  <h3>Ejercicio 3</h3>
  SELECT nombre,
  CASE 
  WHEN email IS NULL THEN 'No tiene email registrado'
  ELSE email
  END AS  email, edad
  from personas;

  
