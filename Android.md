### Documentación de instalación de Android

**Para iniciar con esta instalación es necesario tener la imagen de la versión que queremos instalar, en nuestro caso será la x86**  

**Realizamos la configuración necesaria dentro de VMware, como el número de procesadores, el tamaño de la RAM, el tamaño del disco y la configuración de la tarjeta de red en modo Bridge.**

**Iniciamos la máquina y escogemos la opción que nos permite instalar Android**

<div align="center">
<img src="https://github.com/user-attachments/assets/6e9afc15-f548-454b-ad4e-9fc48bac82f1" alt="Instalar Android" width="600px">
</div>

**Tecleamos la letra C para Crear o Modificar las particiones**

<div align="center">
<img src="https://github.com/user-attachments/assets/e9797db9-b5b6-4ca3-a344-8daed84ef6f6" alt="Particiones" width="600px">
</div>

**En este caso, rechazamos el uso de GPT y crearemos/modificaremos las particiones como si se tratase de Linux (cfdisk)**

<div align="center">
<img src="https://github.com/user-attachments/assets/cffe6d78-e548-4db5-8f38-2023b38389cc" width="600px">
</div>

<div align="center">
<img src="https://github.com/user-attachments/assets/d9c70199-c055-4b0f-827d-4aa906a82627" width="600px">
</div>

**Usaremos el total de nuestro disco para la instalación**

<div align="center">
<img src="https://github.com/user-attachments/assets/46b89b26-860c-443a-b5ea-da3be17c1c10" width="600px">
</div>

**Escogemos ext4 como sistema de archivos (filesystem)**

<div align="center">
<img src="https://github.com/user-attachments/assets/1728d6dc-3a32-408f-9490-9fd340d03aab" width="600px">
</div>

**Instalamos GRUB (Grand Unified Bootloader)**

<div align="center">
<img src="https://github.com/user-attachments/assets/336a2a95-c21b-4e33-9b3b-5105e7a18900" width="600px">
</div>

<div align="center">
<img src="https://github.com/user-attachments/assets/0d0cbc7c-faec-46e5-ad8c-f5ac7e5ffaf6" width="600px">
</div>

**Finalizada la instalación, veremos el menú de arranque GRUB. La primera opción de arranque (resaltada) se selecciona automáticamente, pero Android no arrancará correctamente. 
Para solucionar este problema, seleccionamos la opción de primer arranque y tecleamos la letra E para editar los comandos de arranque**

<div align="center">
<img src="https://github.com/user-attachments/assets/868c3696-5b71-4f38-b099-852efb5fe880" width="600px">
</div>

<div align="center">
<p>Dentro de este comando, debemos reemplazar <i>quiet</i> por <i>nomodeset xforcevesa</i>. Tecleamos la letra B y arrancará Android correctamente</p>
</div>












