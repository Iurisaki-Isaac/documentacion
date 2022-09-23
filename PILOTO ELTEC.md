# INSTALACIÓN

1. Accede al ménu de incio de Windows, busca **Windows PowerShell**, dale clic derecho y ejecuta como administrador

![image](https://user-images.githubusercontent.com/109089231/186736442-ba7e7034-86eb-4021-84d6-06807fd8eb35.png)

2. En PowerShell ejecuta el siguiente comando (copialo, pegalo con clic derecho en la consola y da ENTER):

```powershell
Get-ExecutionPolicy -Scope CurrentUser
```
![image](https://user-images.githubusercontent.com/109089231/186257607-1e5324d4-fe40-4d73-bb4c-8d89f836305b.png)

Si en la consola apareció el mensaje **Unrestricted** puedes continuar al siguiente paso. En caso contrario ejecuta el siguiente comando:

```powershell
Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope CurrentUser
```
Aparecerá un mensaje sobre el **Cambio de directiva de ejecución**. Dale que "si" con una **S** y dando **ENTER** como en el ejemplo de la imagen:

![image](https://user-images.githubusercontent.com/109089231/186732224-a9686348-eec0-4b40-8e38-350fb2cecbcf.png)

3. Dale clic derecho a **installation.ps1** y selecciona **Ejecutar con PowerShell**

![image](https://user-images.githubusercontent.com/109089231/186253331-3eb3a08a-389b-4048-8eb8-658aaf836950.png)

4. Cuando pregunte si quieres permitir que haga cambios en el dispositivo dale que si.
5. Aparecerá un mensaje como el de la siguiente imagen sobre una **Advertencia de seguridad**. Para aceptarlo coloque **Z** y presione ENTER:

![image](https://user-images.githubusercontent.com/109089231/186737780-805a9c3a-0c99-4d87-832c-ef856c813fe1.png)

6. Es posible que pida la instalación de dos paqueterías adicionales: NuGet y PSGallery. Acepta la instalación si es que lo requiere como en el paso 5.
7. Aparecerá un ventana donde puedes seleccionar la carpeta donde se encontrará el programa, selecciona la que desees.

![image](https://user-images.githubusercontent.com/109089231/191273843-21fb368c-a029-4d58-afc2-e9c905d26c18.png)

8. El programa de instalación abrirá una ventana nueva depués de un momento que se verá como la de la imagen:

![image](https://user-images.githubusercontent.com/109089231/192031379-e3d26338-3e74-4e35-9d06-8dd79283c939.png)

En esta ventana de linea de comandos ejecuta el siguiente comando:

```powershell
./dependencias.ps1
```
Como el nombre del programa indica, este sirve para instalar las dependencias. Cuando haya finalizado verá un mensaje como el de la siguiente imagen, puede verificar que efectivamente ha acabado si al final cambio la linea de comandos con una terminación como la circulada en rojo.

![image](https://user-images.githubusercontent.com/109089231/192033143-95460ca7-6741-4e75-a1dc-f7f933a0d807.png)

Ha culminado la instalación, ua puede cerrar todas las ventanas de linea de comandos. En la carpeta que seleccionó, se habrá creado una carpeta llamada files donde se almacenaran los programas, el archivo familias.csv y un ejecutable llamado SolucionDasolab.

![image](https://user-images.githubusercontent.com/109089231/186254669-39286c36-dd4c-42f5-a06a-d3e53a2f0534.png)

9. Al finalizar la instalación cambia las políticas de ejecución de programas al que estaba anteriormente (el mensaje del paso 2) en linea de comandos con el mismo comando al que tenias anteriormente.

Si en el paso 2 el mensaje fue Restricted coloque...

```powershell
Set-ExecutionPolicy -ExecutionPolicy Restricted -Scope CurrentUser
```

Si el mensaje fue Undefined...

```powershell
Set-ExecutionPolicy -ExecutionPolicy Undefined -Scope CurrentUser
```

Si el mensaje fue RemoteSigned

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

Si el mensaje fue AllSigned

```powershell
Set-ExecutionPolicy -ExecutionPolicy AllSigned -Scope CurrentUser
```

10. Ejecuta SolucionDasolab

Puedes cambiar las familias en el archivo **familias.csv**, recuerda siempre colocarlo en la misma carpeta que SolucionDasolab al mismo nivel (no moverlo de carpeta).


# INSTRUCCIONES DE USO DE LA SOLUCIÓN:
1. Dar clic en abrir para desplegar las ventanas de selección de archivos

IMPORTANTE: Asegurate de cerrar todos los archivos que vayas a procesar.

2. Selecciona primero el archivo correspondiente a la semana (El que genera Ariba)
3. Selecciona el archivo que contiene la información de todas las semanas (archivo machote, el que haces tu)
4. El programa procesará el archivo (alrededor de 8 segundos) y lanzará un mensaje de Archivo procesado
5. Abre el archivo machote (que realizas tu) y notarás que ya está actualizado. También verás que se crea un archivo nuevo en la misma carpeta de la solución. Este contiene solo las nuevas hojas de cálcula creadas por la solución.
