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
  
<h2>IF (Si-entonces, sino)</h2>
SELECT IF (1>2,true,false) as Resultado;

SELECT id_producto
IF (cantidad>1,cantidad*precioUnitario,precioUnitario) 
as Total FROM detalles;

SELECT nombre,
  IF (fechaingreso<'2016-12-31',CONCAT  (idEmpleado,'-16'),
    IF (fechaingreso < '2017-12-31',CONCAT  (idEmpleado,'-17'),
      IF (fechaingreso < '2018-12-31',CONCAT  (idEmpleado,'-18'),
        CONCAT  (idEmpleado,'-19') 
        )
      )
   ) as Codigo
   From empleado;

   <h2>IFNULL</h2>
*Si es null escribe texto   
SELECT IFNULL (NULL,"texto") as Resultado;

SELECT nombre, IFNULL (email, telefono) as Contacto
From cliente;
* SELECCIONA EL NOMBRE SI EL EMAIL ES NULL COLOCA EL TELEFONO
SELECT nombre, IFNULL (email, telefono) as Contacto
From cliente;

* SELECCIONA EL NOMBRE SI EL EMAIL ES NULL MUESTRA MENSAJE NO TIENE EMAIL REGISTRDO
SELECT nombre, IFNULL (( SELECT email FROM cliente WHERE id_Cliente = 1), 
'No tiene email registrado') AS Email
From cliente
WHERE id_Cliente = 1;

<h2>NULLIF</h2>

SELECT NULLIF(1,1);

SELECT NULLIF(1,2);

SELECT NULLIF(sELECT precioUnitario FROM producto WHERE id_producto =1),
(SELECT precioUnitario FROM producto WHERE id_producto =2) );






    

   

  
