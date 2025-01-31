### Documentación de instalación de NetBSD

**Para iniciar con esta instalación es necesario tener la imagen de la versión que queremos instalar, en nuestro caso será la 10.0**  

<div align="center">
<img src="https://github.com/user-attachments/assets/90140d7c-6939-4fe3-8ef8-6f6c7ae3abaf" alt="Configuración del teclado">
</div>

**Realizamos la configuración necesaria dentro de VMware, como el número de procesadores, el tamaño de la RAM, el tamaño del disco y la configuración de la tarjeta de red en modo Bridge.**

**Una vez iniciada la máquina, lo primero será escoger el idioma en el que haremos la instalación**

<div align="center">
<img src="https://github.com/user-attachments/assets/f2531b52-2126-43ef-9190-ba4d8e5aeed2" alt="Idioma mensajes de instalación" width="600px">
</div>

**Escogemos tipo de teclado para nuestra máquina virtual**

<div align="center">
<img src="https://github.com/user-attachments/assets/07dd3823-5f6c-473b-9cb7-c7932a7e588c" alt="Tipo de teclado" width="600px">
</div>

**Instalamos NetBSD en el disco duro**

<div align="center">
<img src="https://github.com/user-attachments/assets/e5e1dee5-f3ef-4793-a880-bbf8216cb6e7" alt="Disco duro" width="600px">
</div>

**Instalamos NetBSD en el disco wd0**

<div align="center">
<img src="https://github.com/user-attachments/assets/ad3980b4-5303-4487-b345-9b68c1b82d18" alt="wd0" width="600px">
</div>

**Escogemos el esquema de particionamiento**

<div align="center">
<img src="https://github.com/user-attachments/assets/449f92c1-967b-427c-9cab-9f72246497e6" alt="Esquema de particionamiento" width="600px">
</div>

<div align="center">
  
| GPT (GUID PARTITION TABLE) | MBR (MASTER BOOT RECORD)  |
|----------------------------|-------------------------|
| Es un estándar más nuevo que soporta discos de mayor tamaño (más de 2 TB) y más particiones (hasta 128). GPT es necesario para arrancar desde sistemas UEFI.| Es ampliamente compatible con sistemas más antiguos y firmware BIOS. Soporta discos de hasta 2 TB y permite hasta cuatro particiones primarias (o tres primarias y una extendida).

</div>

**Escogemos dicha geometría**
<div align="center">
<img src="https://github.com/user-attachments/assets/2178e227-8384-4002-8ac4-61fca9745873" alt="Geometría" width="600px">
</div>

**Escogemos la opción "Usar todo el disco", posteriormente, haremos las particiones requeridas**

<div align="center">
<img src="https://github.com/user-attachments/assets/72c1a9f5-9190-438a-966e-ffb2af63770c" width="600px">
</div>

**En el paso siguiente, escogemos la opción que nos permita modificar las particiones y creamos una partición "swap"**

<div align="center">
<img src="https://github.com/user-attachments/assets/e2b843ce-db84-4265-8bf6-2d3661101608" alt="Particiones" width="600px">
</div>

**Escogemos la opción "Usar consola BIOS"**

<div align="center">
<img src="https://github.com/user-attachments/assets/e6327246-8195-4a74-98c1-b126c588d327" alt="BIOS" width="600px">
</div>

**Escogemos la opción "CD/Instalar imagen"**

<div align="center">
<img src="https://github.com/user-attachments/assets/eefe9eef-d310-4d65-b688-da170deec8cc" alt="Instalar imagen" width="600px">
</div>

**El sistema nos dará la opción de asignarle una contraseña al root, podemos dejar el campo vacío**

<div align="center">
<img src="https://github.com/user-attachments/assets/eab6ba29-cc92-41da-aa84-2cebf1810ae3" alt="Contraseña" width="600px">
</div>

**Escogemos la opción que nos permite configurar la red**

<div align="center">
<img src="https://github.com/user-attachments/assets/b514436b-739a-4e2d-a8c9-047cf6df99d8" width="600px">
</div>

**Escogemos la primera interfaz disponible y procedemos a llenar los campos con nuestra configuración de red**

<div align="center">
<img src="https://github.com/user-attachments/assets/591172b9-7a31-4cca-bc2d-d05fa217113a" width="600px">
</div>

<div align="center">
<img src="https://github.com/user-attachments/assets/14890fdd-995c-403f-ac53-53aac616b05b" width="600px">
</div>

**Ahora que tenemos conexión a internet, instalamos los paquetes binarios, esto nos permitira instalar ciertos paquetes más adelante**

<div align="center">
<img src="https://github.com/user-attachments/assets/a89fa3be-ee89-4399-b27b-5f05c9778738" width="600px">
</div>

**Salimos del sistema de instalación de NetBSD y apagamos la máquina virtual, posteriormente, debemos ir a configuraciones, en la sección donde se encuentra la imagen ISO, debemos borrar la imagen**

**Iniciamos la máquina nuevamente, e instalamos Nano y Bash por medio de los siguientes comandos:**
- pkgin install nano
- pkgin install bash
  
Nano es un editor de texto para la terminal y Bash permite ejecutar comandos del sistema, además de crear y ejecutar scripts.

**Actualmente, el teclado no permite ingresar la letra "Ñ", por lo tanto, ejecutamos los siguientes comandos:**
- chsh -s /usr/pkg/bin/bash
Cuando ejecutamos este comando, le estamos diciendo al sistema que queremos usar bash como shell predeterminado. (ChangeShell)
Reiniciamos la máquina y ahora ejecutamos el comando
- nano /.profile
En la parte final de este archivo, ingresamos la siguiente línea: export LANG="en_US.UTF-8"





















