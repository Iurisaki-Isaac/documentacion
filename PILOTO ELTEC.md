# INSTALACIÓN

1. Accede al ménu de incio de Windows, busca PowerShell, dale clic derecho y ejecuta como administrador
2. En PowerShell ejecuta el siguiente comando (copialo, pegalo con clic derecho en la consola y da ENTER):

```powershell
Get-ExecutionPolicy -Scope CurrentUser
```
![image](https://user-images.githubusercontent.com/109089231/186257607-1e5324d4-fe40-4d73-bb4c-8d89f836305b.png)

Si en la consola aparecieron los mensajes...
- RemoteSigned o
- Unrestricted

...puedes continuar al siguiente paso. En caso contrario ejecuta el siguiente comando:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```
![image](https://user-images.githubusercontent.com/109089231/186257532-0dbc1c15-4f58-4711-86df-a7d819d7a8b7.png)

3. Dale clic derecho a installation.ps1 y selecciona Ejecutar con PowerShell

![image](https://user-images.githubusercontent.com/109089231/186253331-3eb3a08a-389b-4048-8eb8-658aaf836950.png)

4. Cuando pregunte si quieres permitir que haga cambios en el dispositivo dale que si
5. Aparecerá un ventana donde puedes seleccionar la carpeta donde se encontrará el programa, selecciona la que desees.

Al culminar la instalción se habrá creado una carpeta llamada files donde se almacenaran los programas, el archivo familias.csv y un ejecutable llamado SolucionDasolab en la carpeta que seleccionaste.

![image](https://user-images.githubusercontent.com/109089231/186254669-39286c36-dd4c-42f5-a06a-d3e53a2f0534.png)

Al finalizar la instalación puedes volver a cambiar las políticas de ejecución de programas en linea de comandos con el mismo comando:

```powershell
Set-ExecutionPolicy -ExecutionPolicy [COLOCA AQUI Restricted O Undefined DEPENDIENDO DE LO QUE TUVIERAS ANTES SIN LOS CORCHETES] -Scope CurrentUser
```

6. Ejecuta SolucionDasolab

Puedes cambiar las familias en el archivo familias.csv, recuerda siempre colocarlo en la misma carpeta que SolucionDasolab al mismo nivel (no moverlo de carpeta).


# INSTRUCCIONES DE USO DE LA SOLUCIÓN:
1. Dar clic en abrir para desplegar las ventanas de selección de archivos

IMPORTANTE: Asegurate de cerrar todos los archivos que vayas a procesar.

2. Selecciona primero el archivo correspondiente a la semana (El que genera Ariba)
3. Selecciona el archivo que contiene la información de todas las semanas (archivo machote, el que haces tu)
4. El programa procesará el archivo (alrededor de 8 segundos) y lanzará un mensaje de Archivo procesado
5. Abre el archivo machote (que realizas tu) y notarás que ya está actualizado.


# Documentación (para los desarrolladores)

## eltec_excel_parser_py

Repositorio creado para parsear y reacomodar el archivo de provedoor acorde al archivo propuesto por david
Del archivo de david parsear y reacomodar informacion para archivo de presentacion ante direccion

## Para levantar el contenedor

### Creacion de imagen

docker build -t python_pandadocs_prueba .

### Correr contenedor (se creara, correra el proces y se eliminara al terminar)

docker run -it --rm --name prueba1 python_pandadocs_prueba
