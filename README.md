# Informe de laboratorio

## Introducción
El objetivo principal de este laboratorio fue instalar y configurar distintas distribuciones de sistemas operativos Unix y Windows como parte de la configuración de la plataforma. También se buscó familiarizarse con el uso de software de virtualización. Este laboratorio nos proporcionó la oportunidad de aprender y aplicar conceptos clave en la administración de sistemas y redes dentro de un entorno práctico.

Durante el laboratorio, utilizamos el laboratorio de computación de la institución, que contaba con equipos, acceso a internet y software de virtualización. Cada grupo de estudiantes trajo imágenes de sistemas operativos y dispositivos de almacenamiento externos para completar las tareas asignadas. Se realizaron diversas actividades que abarcaron desde la instalación de sistemas operativos hasta la configuración de usuarios y redes.

## Desarrollo del tema 
[Ver información sobre Slackware](Slackware.md)

### Marco teórico
Unix-Based Server Setup	
a. Server Installation and Configuration
•	What files are generated during installation in each virtualization software, and what are their purposes?
Archivos comunes en todas las máquinas virtuales de VMWare:
Archivos de configuración:
.vmx - El archivo principal de configuración que contiene todos los ajustes de la máquina virtual
.vmxf - Archivo de configuración adicional con metadatos de la máquina virtual
.nvram - Almacena la configuración del BIOS/UEFI de la máquina virtual

Archivos de almacenamiento:
.vmdk - El disco virtual que contiene el sistema operativo y datos. Contiene tanto los datos del disco como los descriptores
-flat.vmdk - Contiene los datos reales del disco virtual
.vmem - Archivo de memoria cuando la máquina está suspendida

Archivos de estado:
.vmsd - Almacena información sobre snapshots
.vmsn - Archivos de snapshot individuales
.vmss - Archivo del estado guardado cuando la máquina está suspendida


	Archivos para Slackware:
Archivos de sistema: 
o	/etc/inittab - Controla el proceso de inicio del sistema
o	/etc/fstab - Configuración de puntos de montaje
o	/etc/passwd y /etc/shadow - Información de usuarios y contraseñas
o	/etc/hostname - Nombre del host
o	/etc/resolv.conf - Configuración DNS
o	/var/log/messages – Almacena todos los eventos de autenticación al sistema

Archivos de gestión de paquetes:
o	/var/log/packages/* - Registro de todos los paquetes instalados
o	/var/log/scripts/* - Scripts de instalación de paquetes
o	/etc/slackpkg/slackpkg.conf - Configuración del gestor de paquetes

Scripts de inicio:
o	/etc/rc.d/rc.M - Script principal de inicio
o	/etc/rc.d/rc.inet1 - Configuración de red
o	/etc/rc.d/rc.local - Scripts personalizados de inicio

Archivos para NetBSD:
Archivos de sistema:
o	/etc/master.passwd - Base de datos principal de usuarios
o	/etc/pwd.db y /etc/spwd.db - Bases de datos de contraseñas
o	/etc/fstab - Tabla de sistemas de archivos
o	/etc/hostame.if0 - Configuración de la interfaz de red
o	/var/log/authlog– Almacena todos los eventos de autenticación al sistema
Archivos de configuración:
o	/etc/rc.conf - Configuración principal del sistema
o	/etc/nsswitch.conf - Configuración de servicios de nombres
o	/etc/mk.conf - Configuración de compilación
Gestión de paquetes:
o	/var/db/pkg/ - Base de datos de paquetes instalados
o	/usr/pkg/etc/ - Configuración de paquetes instalados
o	/var/db/pkgin/ - Base de datos del gestor de paquetes pkgin

•	What is the file system? Which one did you use during installation? What are its characteristics?
Un sistema de archivos (FS) es la estructura que un sistema operativo utiliza para organizar y almacenar archivos en un dispositivo de almacenamiento (un disco duro, por ejemplo). El sistema de archivos gestiona cómo los datos se almacenan, se recuperan y se organizan en dispositivos de almacenamiento.

Slackware
ext4 (Fourth Extended Filesystem):
Características:
Mejor rendimiento y fiabilidad: ext4 es el sucesor de ext3 y mejora el rendimiento y la fiabilidad.
Soporte para archivos grandes: Ext4 soporta volúmenes de hasta 1 exabyte y archivos de hasta 16 terabytes.
Journaling: Al igual que ext3, ext4 usa journaling para prevenir la corrupción de datos, lo que mejora la recuperación en caso de un apagón inesperado o fallo del sistema.
Optimización de espacio: ext4 mejora la eficiencia en la distribución de espacio libre y la gestión de archivos.
Compatibilidad: ext4 es totalmente compatible con ext3, lo que facilita la migración.

NetBSD
FFS (Fast File System):

Características:
Diseñado para UNIX: FFS fue diseñado inicialmente para sistemas operativos tipo UNIX.
Compatibilidad: Es el sistema de archivos más utilizado en sistemas BSD, incluidos NetBSD.
Journaling: No tiene journaling (aunque es posible habilitarlo en algunos casos mediante el uso de un sistema como UFS2).
Bloques: FFS organiza los archivos en bloques de tamaño fijo, lo que permite un rendimiento eficiente.

Journaling: En un sistema de archivos con journaling, el sistema registra (o "escribe en un diario") las operaciones de modificación antes de realizar cualquier cambio en los archivos o en la estructura del sistema de archivos.

•	Is it possible to convert a VMware virtual machine to VirtualBox and vice versa? 
De VMWare a VirtualBox:
1.	En VMware, exportar la máquina virtual como OVF(Open Virtualization Format)/OVA(Open Virtual Appliance)
2.	En VirtualBox, importar el archivo OVF/OVA
De VirtualBox a VMWare:
1.	En VirtualBox, exportar la máquina virtual como OVF(Open Virtualization Format)
2.	En VMWare, importar el archivo OVF
3.	Si se importa la máquina virtual desde Virtual Box como OVA, se debe pasar por una herramienta que convierta el archivo OVA a VMX.



•	Initially, set up network configurations automatically using DHCP and configure the machines in bridge mode. What do ”Bridge Mode” and ”NAT Mode” mean? 
Bridge Mode: La máquina virtual actúa como si fuera una computadora física más dentro de la misma red que el host. Esto significa que la máquina virtual tiene su propia dirección IP dentro de la red local, y puede comunicarse con otros dispositivos de la red como si fuera un equipo físico independiente. La máquina virtual obtiene una dirección IP del mismo rango que el host (del router o del servidor DHCP de la red local).
NAT(Network Address Translation) Mode: La máquina virtual se conecta a la red a través del host, pero utiliza una dirección IP privada que el host "traduce" a una dirección IP pública. El host actúa como un router. Esto significa que la máquina virtual no es directamente accesible desde otras computadoras en la red externa, pero puede acceder a Internet a través de la conexión de red del host. Esto puede ser beneficioso cuando se intenta aislar la máquina virtual de posibles ataques o cuando hay direcciones IP limitadas disponibles.
What IP address was assigned to the machine: 10.2.78.50

•	Compare the installation experiences of the operating systems.

b. Understanding and Managing Operating Systems 
•	What is the directory structure of the installed operating systems? List the directories, describe their content, and compare Slackware and NetBSD.
/ (Root):
Descripción: El directorio principal, la raíz del sistema de archivos. Todos los demás directorios son subdirectorios de este.
Contenido: Todos los directorios del sistema se encuentran aquí.

/bin:
Descripción: Contiene los binarios esenciales necesarios para el funcionamiento básico del sistema.
Contenido: Comandos esenciales como ls, cp, mv, cat, etc.

/sbin:
Descripción: Contiene binarios del sistema utilizados generalmente para tareas de mantenimiento o recuperación, a menudo por el usuario root.
Contenido: Comandos como fsck, reboot, ifconfig, etc.

/etc:
Descripción: Contiene los archivos de configuración global del sistema.
Contenido: Archivos de configuración para la red, servicios del sistema, usuarios, y scripts de inicio, como /etc/passwd, /etc/fstab, /etc/network.

/dev:
Descripción: Contiene los archivos de dispositivo que representan los dispositivos de hardware del sistema.
Contenido: Archivos de dispositivos como /dev/sda (dispositivos de disco), /dev/tty (terminales), etc.

/home:
Descripción: Contiene los directorios personales de los usuarios.
Contenido: Cada usuario tiene un directorio bajo /home (por ejemplo, /home/usuario).

/var:
Descripción: Contiene datos variables, como registros (logs), bases de datos y archivos de cola.
Contenido: Archivos de registro en /var/log, colas de correo, archivos temporales, y datos de ejecución.

/tmp:
Descripción: Contiene archivos temporales que pueden ser creados por las aplicaciones.
Contenido: Archivos temporales que pueden eliminarse al reiniciar o apagar el sistema.

/usr:
Descripción: Contiene programas, bibliotecas y documentación relacionada con el usuario.
Contenido: Subdirectorios como /usr/bin (binarios de usuario), /usr/lib (bibliotecas), /usr/share (datos compartidos), /usr/include (encabezados).

/lib:
Descripción: Contiene las bibliotecas compartidas esenciales y módulos del núcleo.
Contenido: Bibliotecas necesarias para que los binarios en /bin y /sbin funcionen (por ejemplo, /lib/libc.so).

/mnt:
Descripción: Un punto de montaje temporal para dispositivos de almacenamiento, como discos duros externos o unidades USB.
Contenido: Dispositivos externos montados temporalmente (por ejemplo, /mnt/usb).

/media:
Descripción: Similar a /mnt, utilizado para montar medios removibles como CD, DVD y dispositivos USB.
Contenido: Medios removibles, como /media/usb o /media/cdrom.


•	What are system log files?
Los archivos de registro del sistema son archivos donde se almacenan mensajes generados por el sistema operativo y diversas aplicaciones. Estos archivos permiten monitorear eventos importantes, errores, advertencias y otras actividades del sistema.
•	 What is syslog? What are the main files related to syslog? What types of information are recorded in log files? What is their structure? Provide five examples of logged events. Does syslog work on the installed operating systems?
Syslog es un protocolo estándar para el registro de eventos en sistemas Unix y similares. Permite que las aplicaciones y el sistema operativo envíen mensajes de registro a un servidor de registros centralizado o a archivos locales.

/var/log/syslog → Contiene mensajes generales del sistema.
/var/log/auth.log → Registra intentos de autenticación y acceso al sistema.
/var/log/kern.log → Contiene mensajes del kernel.
/var/log/dmesg → Muestra los eventos generados durante el arranque del sistema.
/var/log/mail.log → Almacena registros de correos electrónicos.

Estructura de un archivo de log: Fecha y hora | Nombre del host | Proceso o servicio | Mensaje del evento

•	How do permissions work in the installed operating systems? Explain how to modify permissions using character and numeric representations.

En Linux y Unix, los permisos se definen para usuarios, grupos y otros, y determinan quién puede leer, escribir o ejecutar un archivo o directorio.
Representación en caracteres: 
o	r → Lectura (read)
o	w → Escritura (write)
o	x → Ejecución (execute)
Se usa + para dar permisos y – para quitarlos.
	Representación en números:
o	r = 4
o	w = 2
o	x = 1
o	Owner (u)
o	Group (g)
o	Others (o)

chmod [who][operator][permissions] filename

Windows Server Installation and Configuration – Phase 2
•	How are permissions managed in Windows Server?
Los permisos en Windows Server se administran a través del Sistema de archivos NTFS y las políticas de grupo (Group Policy). Se pueden configurar permisos a nivel de archivos y carpetas utilizando la pestaña "Seguridad" en las propiedades del archivo o carpeta, donde se pueden asignar permisos a usuarios o grupos. También se pueden administrar permisos en el Active Directory mediante el control de acceso basado en roles (RBAC).
•	What is the directory structure of Windows Server?
C:\Windows – Contiene archivos del sistema operativo.
C:\Program Files – Almacena aplicaciones instaladas.
C:\Program Files (x86) – Para aplicaciones de 32 bits en sistemas de 64 bits.
C:\Users – Contiene perfiles de usuario.
C:\Windows\System32 – Archivos esenciales del sistema y ejecutables.
C:\Windows\SysWOW64 – Versiones de 32 bits de archivos de System32 en sistemas de 64 bits.
C:\inetpub – Directorio para servidores web en IIS (Internet Information Services).
C:\Windows\Logs – Archivos de registro del sistema y de eventos
•	What is the Windows Registry? What is its purpose? How is it edited? What type of information does it store?
El Registro de Windows (Windows Registry) es una base de datos jerárquica donde el sistema operativo y las aplicaciones almacenan configuraciones y ajustes.

Su propósito es mantener información crucial sobre el sistema, como configuraciones de hardware, perfiles de usuario y preferencias de software.

Se puede editar utilizando la herramienta Regedit:
Presionar Win + R, escribir regedit y presionar Enter.
Navegar por la estructura en forma de árbol de claves y valores.
Modificar valores según sea necesario (con precaución).
•	How are Windows Server logs accessed?
Se puede acceder a los logs en la carpeta: C:\Windows\System32\winevt\Logs
O mediante PowerShell: Get-EventLog -LogName System

•	Identify server log events such as failed login attempts, user access, and unauthorized actions (e.g., attempting to delete a file without permission). 
Código para ver accesos fallidos: 
$logfile = "security"

$failedAttempts = Get-WinEvent -LogName $logfile | Where-Object { $_.Id -eq 4625 }

Write-Host "Intentos fallidos de acceso al usuario Administrator:"

$failedAttempts | ForEach-Object {
  $eventTime = $_.TimeCreated
  $user = $_.Properties[5].value
  if ($user -eq "Administrator") {
    Write-Host "$eventTime - Usuario: $user"
  }
}

$total = ($failedAttempts | Where-Object { $_.Properties[5].Value -eq "Administrator" }).Count
Write-Host "Cantidad total de intentos fallidos: $total"

### Uso y aplicaciones

## Conclusiones 
### Experiencia de Instalación y Configuración

1. *Instalación de Sistemas Operativos*:
   - La instalación de Linux Slackware y NetBSD en modo experto, sin entorno gráfico, nos permitió entender mejor los componentes esenciales para el funcionamiento básico del sistema.
   - La instalación de Windows Server, tanto en versión gráfica como sin interfaz gráfica, nos mostró las diferencias en la gestión de sistemas operativos Unix y Windows.

2. *Configuración de Red*:
   - Configurar las direcciones IP, la máscara de subred, y el gateway de manera manual y automática nos proporcionó una comprensión más profunda de los conceptos de Bridge Mode y NAT Mode.
3. *Manejo de Usuarios y Permisos*:
   - La creación de usuarios y grupos, así como la asignación de permisos específicos, nos ayudó a entender la administración de sistemas y la importancia de la seguridad en la gestión de usuarios.

4. *Pruebas de Conectividad*:
   - Realizar pruebas de conectividad con comandos como ping nos permitió verificar la funcionalidad de la red y la configuración correcta de las IPs.

### Comparaciones y Observaciones

- *Estructura de Directorios*:
  - Comparar las estructuras de directorios y los archivos de configuración en Slackware y NetBSD nos dio una visión clara de cómo se organizan y administran los archivos en diferentes sistemas Unix.
  
- *Registros del Sistema (Logs)*:
  - Aprendimos sobre la importancia de los archivos de registro (logs) y cómo utilizar syslog para monitorear eventos en los sistemas instalados.

- *Permisos*:
  - La modificación de permisos utilizando representaciones numéricas y de caracteres destacó la flexibilidad y control que se puede tener sobre los recursos del sistema.

### Reflexión Final

Este laboratorio fue una experiencia enriquecedora que no solo nos permitió adquirir habilidades técnicas, sino también mejorar nuestra capacidad para resolver problemas y trabajar en equipo. El conocimiento adquirido sobre la virtualización y la configuración de sistemas operativos es fundamental para cualquier profesional en el ámbito de la administración de sistemas y redes.


## Bibliografía 
