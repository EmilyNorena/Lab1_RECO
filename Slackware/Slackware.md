### Documentacion de instalacion de slackware
**Para iniciar con esta instalacion es necesario tener la imagem de la version que queremos instalar, en nuestro caso sera la 15.0**
**Realizamos la configuracion necesaria dentro de VMware, como el numero de procesadores, el tamaño de la ram, el tamaño del disco y la configuracion de la tarjeta de red.**

**Una vez iniciada la maquina, lo primero sera la configuracion del teclado, donde seleccionaremos "qwerty/la-latin1.map"**

![imagen](https://github.com/user-attachments/assets/1a1fa3ac-d721-4968-a141-230de605ca0e)

**Hacemos un login como "root"**

![imagen](https://github.com/user-attachments/assets/5f489209-94c3-40e3-99b9-df2765859a71)

**Iniamos con las particiones del disco de la maquina, para ello ingresamos el comando "cfdisk"**

![imagen](https://github.com/user-attachments/assets/1664db1f-5e2d-4365-a654-29ef52cb4614)

**Luego seleccionamos la opcion "gpt"**

![imagen](https://github.com/user-attachments/assets/f88365bb-9a60-4dc9-a542-474a47a9ec83)

**Realizamos dos particiones, una de tipo swap y la otra standard**

![imagen](https://github.com/user-attachments/assets/c7c0cafe-17c6-43ff-a956-b23bd615727d)

**Una vez teminada esta parte, ingresamos el comando "setup"**

![imagen](https://github.com/user-attachments/assets/ba0f32a9-76a1-463e-a2e8-3cc6bad7ef06)

**En la primer parte le daremos "ok"**

![imagen](https://github.com/user-attachments/assets/0a922213-5b51-4d34-955b-ab9b842a68bb)

**Nuevamente le daremos "ok"**

![imagen](https://github.com/user-attachments/assets/6c71c867-99cb-46b5-a0db-8eb7f6ca4c14)

**Seleccionamos "ext4" como tipo de sistema de archivos**

![imagen](https://github.com/user-attachments/assets/f720471f-408f-4108-8664-294cf466ca0c)

**Elegimos la primer opcion ya que estamos usando una "iso"**

![imagen](https://github.com/user-attachments/assets/d7305195-2d0f-4eaf-aac4-380577152cbb)

**Luego elegimos el modo de instalacion "expert" para tener un mayor control de que estamos instalando**

![imagen](https://github.com/user-attachments/assets/2322c88f-9bad-410b-a7db-c2d44378c405)

**En este punto elegimos los siguientes paquetes de instalacion:

# Categorías de Paquetes

## Categoría: `a`

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

---

## Categoría: `ap`

<div align="center">

| Paquete             | Paquete             |
|---------------------|---------------------|
| slackpkg            | nano                |
| sudo                |                     |

</div>


## Categoría: `d`

| Paquete             | Paquete             |
|---------------------|---------------------|
| perl                |                     |

---

## Categoría: `L`

| Paquete             | Paquete             |
|---------------------|---------------------|
| libunistring       | ncurses             |

---

## Categoría: `n`

| Paquete             | Paquete             |
|---------------------|---------------------|
| ca-certificates     | iputils             |
| iproute2            | net-tools           |
| libmnl              | npt                 |
| network-scripts     | openssl             |
| openssh             | wget                |
| gnupg               |                     |



**Instalamos LILO en modo "simple"**

![imagen](https://github.com/user-attachments/assets/8ba0f6a4-6013-47ab-9d86-50ff7de2b49f)
