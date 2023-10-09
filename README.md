# OnbasePurgeTool
La siguiente aplicación permite a un administrador del sistema localizar documentos por fecha y tipo de documento, y eliminarlos o purgarlos.

# Configuración

A continuación se describen los cambios que se deben realizar en el archivo **Configuraciones.xml**

Cambiar el nombre del archivo "**Configuraciones.xml.example**" por "**Configuraciones.xml**"
Abrir el archivo "**Configuraciones.xml**" con un editor de texto y modificar o agregar una nueva configuración con la siguiente estructura
```xml
<cnf id="NOMBRE_AMBIENTE"> <!-- Sirve para mostrar en la lista dentro de la aplicación, ejemplo CLIENTE1_DEV --> 
  <ServicePath>http://localhost/AppServer/Service.asmx</ServicePath> <!-- URL del AppServer --> 
  <DataSource>OnBase</DataSource> <!-- ODBC --> 
  <Username>MANAGER</Username> <!-- Usuario de onbase--> 
  <Password>password</Password> <!-- Contraseña de usuario onbase --> 
</cnf>
```
Reemplaza los valores dentro de las etiquetas por tu configuración de conexión


# Manual
A continuación se proporcionan instrucciones sobre como utilizar la aplicación

1. Inicie la aplicación ejecutando **Onbase Purge Tool.exe**
2. En la pantalla busque la lista desplegable y seleccione el ambiente donde se quiere conectar
3. Haga clic en el botón "**Conectarse**" y espere a que muestre el usuario y el sessión ID de la conexión
4. Una vez conectado puede seleccionar un Document Type Group de la lista
5. Aparecerán la lista de Document Types de ese Document Type group
6. Debe seleccionar un rango de fechas
7. Debe Selecciónar la acción que requiera (Listar y contar, Eliminar o Purgar)
8. Haga clic en ejecutar

**Nota: Eliminar permite desde el cliente grueso recuperar el documento pero si escoge la acción de purgar no será posible recuperarlos.**
