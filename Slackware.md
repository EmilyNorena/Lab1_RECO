### Documentación de instalación de Slackware

**Para iniciar con esta instalación es necesario tener la imagen de la versión que queremos instalar, en nuestro caso será la 15.0**  
**Realizamos la configuración necesaria dentro de VMware, como el número de procesadores, el tamaño de la RAM, el tamaño del disco y la configuración de la tarjeta de red.**

**Una vez iniciada la máquina, lo primero será la configuración del teclado, donde seleccionaremos "qwerty/la-latin1.map"**

<div align="center">
<img src="https://github.com/user-attachments/assets/1a1fa3ac-d721-4968-a141-230de605ca0e" alt="Configuración del teclado">
</div>

**Hacemos un login como "root"** 

<div align="center">
<img src="https://github.com/user-attachments/assets/5f489209-94c3-40e3-99b9-df2765859a71" alt="Login como root">
</div>

**Iniciamos con las particiones del disco de la máquina, para ello ingresamos el comando "cfdisk"**

<div align="center">
<img src="https://github.com/user-attachments/assets/1664db1f-5e2d-4365-a654-29ef52cb4614" alt="Comando cfdisk">
</div>

**Luego seleccionamos la opción "gpt"**

<div align="center">
<img src="https://github.com/user-attachments/assets/f88365bb-9a60-4dc9-a542-474a47a9ec83" alt="Selección de GPT">
</div>

**Realizamos dos particiones, una de tipo swap y la otra estándar**

<div align="center">
<img src="https://github.com/user-attachments/assets/c7c0cafe-17c6-43ff-a956-b23bd615727d" alt="Particiones">
</div>

**Una vez terminada esta parte, ingresamos el comando "setup"**

<div align="center">
<img src="https://github.com/user-attachments/assets/ba0f32a9-76a1-463e-a2e8-3cc6bad7ef06" alt="Comando setup">
</div>

**En la primera parte le daremos "ok"**

<div align="center">
<img src="https://github.com/user-attachments/assets/0a922213-5b51-4d34-955b-ab9b842a68bb" alt="Primera confirmación">
</div>

**Nuevamente le daremos "ok"**

<div align="center">
<img src="https://github.com/user-attachments/assets/6c71c867-99cb-46b5-a0db-8eb7f6ca4c14" alt="Segunda confirmación">
</div>

**Seleccionamos "ext4" como tipo de sistema de archivos**

<div align="center">
<img src="https://github.com/user-attachments/assets/f720471f-408f-4108-8664-294cf466ca0c" alt="Selección de ext4">
</div>

**Elegimos la primera opción ya que estamos usando una "iso"**

<div align="center">
<img src="https://github.com/user-attachments/assets/d7305195-2d0f-4eaf-aac4-380577152cbb" alt="Selección de ISO">
</div>

**Luego elegimos el modo de instalación "expert" para tener un mayor control de qué estamos instalando**

<div align="center">
<img src="https://github.com/user-attachments/assets/2322c88f-9bad-410b-a7db-c2d44378c405" alt="Modo de instalación expert">
</div>

**En este punto elegimos los siguientes paquetes de instalación:**

---

## Categoría: `a`

<div align="center">

| Paquete             | Paquete             | Paquete             | Paquete             | Paquete             |
|---------------------|---------------------|---------------------|---------------------|---------------------|
| aaa_base            | kernel-modules      | aaa_glibc-solibs    | kmod                | aaa_libraries       |
| aaa_terminfo        | libgudev            | acl                 | libpwquality        | attr                |
| bash                | lilo                | logrotate           | bin                 | mkinitrd            |
| bzip2               | nvi                 | coreutils           | openssl-solibs      | cpio                |
| cracklib            | pam                 | dbus                | pkgtools            | dcron               |
| procps-ng           | devs                | sed                 | dialog              | shadow              |
| e2fsprogs           | sharutils           | elogind             | syslinux            | etc                 |
| sysklogd            | eudev               | sysvinit            | file                | sysvinit-scripts    |
| findutils           | tar                 | gawk                | util-linux          | glibc-zoneinfo      |
| which               | xz                  | gzip                | hostname            | kbd                 |
| kernel-firmware     | kernel-generic      | kernel-huge         |                     |                     |

</div>

---

## Categoría: `ap`

<div align="center">

| Paquete             | Paquete             |
|---------------------|---------------------|
| slackpkg            | nano                |
| sudo                |                     |

</div>

---

## Categoría: `d`

<div align="center">

| Paquete             | Paquete             |
|---------------------|---------------------|
| perl                |                     |

</div>

---

## Categoría: `L`

<div align="center">

| Paquete             | Paquete             |
|---------------------|---------------------|
| libunistring       | ncurses             |

</div>

---
## Categoría: `n`

<div align="center">

| Paquete             | Paquete             |
|---------------------|---------------------|
| ca-certificates     | iputils             |
| iproute2            | net-tools           |
| libmnl              | npt                 |
| network-scripts     | openssl             |
| openssh             | wget                |
| gnupg               |                     |

</div>


**Instalamos LILO en modo "simple"**

<div align="center">
<img src="https://github.com/user-attachments/assets/8ba0f6a4-6013-47ab-9d86-50ff7de2b49f" alt="Instalación de LILO">
</div>

**Elegimos "standard"**

<div align="center">
<img src="https://github.com/user-attachments/assets/4229b57c-53a9-46dc-b0d2-78ad3f545b72" alt="Selección de standard">
</div>

**En ruta de instalación elegimos "MBR"**

<div align="center">
<img src="https://github.com/user-attachments/assets/edf633b7-e019-46dd-8927-722168749182" alt="Ruta de instalación MBR">
</div>

**En nombre de dominio ponemos "escuelaing.edu.co"**

<div align="center">
<img src="https://github.com/user-attachments/assets/7ec05c4d-4b27-45ed-8250-3d6c16c62c07" alt="Nombre de dominio">
</div>

**Elegimos "static IP"**

<div align="center">
<img src="https://github.com/user-attachments/assets/f94660fb-f22d-49aa-a655-997a059082e3" alt="Selección de Static IP">
</div>

**Escogemos la opción "nvi"**

<div align="center">
<img src="https://github.com/user-attachments/assets/9ac6b648-8c78-4b8c-92dd-67899c5bd158" alt="Selección de nvi">
</div>

**En IPv4 agregamos la IP asignada en el laboratorio**

<div align="center">
<img src="https://github.com/user-attachments/assets/5029ff7f-61c0-4bf8-a450-56698cd15e9e" alt="Configuración de IPv4">
</div>

**De GATEWAY agregamos 10.2.65.1**

<div align="center">
<img src="https://github.com/user-attachments/assets/abc2f6f2-c2d9-44bd-a272-f82b2f9acda4" alt="Configuración de Gateway">
</div>

**Finalmente nos queda algo así**

<div align="center">
<img src="https://github.com/user-attachments/assets/1ef3b218-58b4-4e67-adf5-d1644548f759" alt="Configuración final">
</div>

**Y reiniciamos**

**Luego para hacer la creacion de los usuarios pedidos en la guia usamos los siguientes comandos, primero creamos los grupos:**

![imagen](https://github.com/user-attachments/assets/475c3fee-023a-49db-95c7-f48a545a08ef)

**Creamos los usuarios**

![imagen](https://github.com/user-attachments/assets/764eeed5-3868-42f3-be86-4d4074555bba)

![imagen](https://github.com/user-attachments/assets/2e4a5d09-6880-4f34-a8cb-f8bc459c3556)
