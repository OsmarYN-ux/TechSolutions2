#############################################################
# README: APLICACIÓN EMPRESARIAL TECH SOLUTIONS (.NET WPF)
#############################################################

Este archivo contiene las instrucciones de ejecución, pruebas y el despliegue final para el proyecto empresarial Tech Solutions, desarrollado con arquitectura N-Capas, WPF y SQL Server.

=============================================================
1. REQUISITOS DE EJECUCIÓN
=============================================================

- Entorno: Microsoft Visual Studio (para compilar el código fuente).
- Base de Datos: Acceso a una instancia local de SQL Server (ej., (localdb)\MSSQLLOCALDB) con la base de datos 'TechDB' creada.

=============================================================
2. CREDENCIALES DE PRUEBA (Autenticación)
=============================================================

Para iniciar sesión y validar la funcionalidad de Login/Hashing, utilice el siguiente usuario:

USUARIO: admin
CONTRASEÑA: [Debe usar la clave plana que generó el hash SHA256] 
           (Ejemplo: Si el hash es 'a665a459...', la clave plana es 'admin123')

FUNCIONALIDAD CLAVE: Una vez dentro, el usuario 'admin' debe tener acceso al menú 'Reportes' (Autorización).

=============================================================
3. PRUEBAS FUNCIONALES CLAVE
=============================================================

A. PRUEBA DE TRANSACCIÓN (Venta):
   - Pasos: Ir a Transacciones -> Registrar Venta. Ingresar IDs válidos (ej., Cliente: 1, Vendedor: 1) y agregar un producto (doble click).
   - Resultado Esperado: Mensaje de "Venta registrada con éxito (COMMIT ejecutado)".

B. PRUEBA DE REPORTES (SP y LINQ):
   - Pasos: Ir a Reportes, seleccionar un rango de fechas y hacer clic en "Generar Reporte".
   - Resultado Esperado: La lista de ventas se carga en el DataGrid (llamada al SP) y aparece un resumen del Total de Ventas (Uso de LINQ).

C. PRUEBA DE CRUD/LINQ:
   - Pasos: Ir a Gestión -> Productos.
   - Resultado Esperado: La lista debe cargarse (uso del ProductoRepository). El filtrado en el TextBox superior debe funcionar en tiempo real (uso de LINQ).

=============================================================
4. ARTEFACTOS DE ENTREGA (Archivos Finales)
=============================================================

1. CÓDIGO FUENTE: Carpeta de la solución VS con todos los proyectos (UI, BLL, DAL, Models).
2. INSTALADOR: Archivo .msi generado por el Setup Project (TechSolutions.Setup).
3. DOCUMENTACIÓN: Informe técnico (PDF) que incluye todos los diagramas UML (N-Capas, Secuencia, Actividad, Despliegue, etc.).
4. SCRIPTS SQL: Archivos .sql necesarios para la creación de la base de datos (DDL) y la inserción de datos iniciales.

#############################################################