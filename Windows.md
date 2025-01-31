### Creación de la Máquina Virtual de Windows

### Máquina sin interfaz

Iniciamos con una configuración básica, colocándole su respectivo nombre.



Le configuramos un tamaño básico para la RAM.



Le asignamos 15GB de almacenamiento.



Configuramos la red.


Podemos seleccionar el teclado en español Colombia.

![Captura5](https://github.com/user-attachments/assets/09666b1a-a346-428e-801a-67a577c4ad2b)

En este caso, como se quiere instalar sin interfaz gráfica, seleccionamos la versión Standard.

![imagen](https://github.com/user-attachments/assets/da526663-3a63-4d8d-9169-3b0ce9e4f3b3)

Aceptamos los términos.

![imagen](https://github.com/user-attachments/assets/beb2b444-5014-46a0-b992-fe7cb0feb85e)

Elegimos la instalación personalizada.

![Captura28](https://github.com/user-attachments/assets/3bfaa0ff-3db6-4a55-b7bc-d87f10b517b5)

Seleccionamos el disco recién creado.

![Captura9](https://github.com/user-attachments/assets/9e37702e-21c7-41d0-b946-661ee5b2adba)

Esperamos un rato a que instale.

![imagen](https://github.com/user-attachments/assets/d31c719c-12b7-4dce-bc0a-7d3ffde4d45a)

Seleccionamos "OK" para asignarle una contraseña.

![Captura11](https://github.com/user-attachments/assets/4ad02504-8ffa-4767-a754-9be30ab18d27)

Digitamos una contraseña "root1234" y presionamos ENTER.

![Captura12](https://github.com/user-attachments/assets/68464a4f-e21b-42e1-8995-654d16c7578b)

Esperamos que inicie.

![Captura13](https://github.com/user-attachments/assets/a1fbd167-76ff-48ca-92aa-930070987e8e)

Iniciamos la configuración de red, eligiendo la opción 8.

![Captura14](https://github.com/user-attachments/assets/efca80cd-8537-4427-8fa9-6c3116fa24b9)

Seleccionamos la opción 1.

![Captura15](https://github.com/user-attachments/assets/89a8c6a5-44a8-46c3-9ae0-f093c5cf0438)

Nuevamente seleccionamos la opción 1 para configurar la red.

![Captura16](https://github.com/user-attachments/assets/e3cce41c-8481-438f-b00a-61192070f768)

Ingresamos "S" para continuar.

![Captura17](https://github.com/user-attachments/assets/bbee3e43-30ff-4367-841d-a70dead329ec)

Escribimos la IP dada por el laboratorio.\
\*\
Ingresamos la máscara también dada por el laboratorio.\
\*\
Escribimos el "Gateway".\
\*\
Después de presionar ENTER, ingresamos nuevamente al menú seleccionando la opción 8.\
\*\
Accedemos a la configuración de DNS.\
\*\
Ingresamos el DNS proporcionado por la guía.\
\*\
Salimos de la configuración eligiendo la opción 15.\
\*\
Iniciamos las pruebas de ping, empezando por "8.8.8.8".\
\*\
Realizamos las pruebas con los demás valores.\
\*\
Procedemos a agregar los 3 usuarios solicitados.\
\*\
Asignamos a cada uno un grupo distinto para que tengan diferentes permisos.\
\*\
Finalmente, confirmamos que cada usuario esté dentro de su grupo correspondiente.\
\*

### Máquina con interfaz

Realizamos los primeros pasos de la misma manera que en la anterior.\
\*\
\*\
\*\
\*\
\*\
\*\
En este punto, a diferencia de la máquina anterior, seleccionamos "Standard (Desktop Experience)".\
\*\
Seleccionamos la instalación "Custom".\
\*\
Elegimos el disco recién creado.\
\*\
Esperamos a que termine la instalación.\
\*\
Iniciamos la configuración asignando una contraseña para el perfil de Administrador "Root1234".\
\*\
\*\
Después de acceder, nos encontramos en el menú principal.\
\*\
Para crear los demás usuarios, entramos en configuración.\
\*\
Accedemos a "Accounts".\
\*\
Seleccionamos "Other Users".\
\*\
Hacemos clic en "Add".\
\*\
Ingresamos a la carpeta de Users.\
\*\
Hacemos clic derecho y seleccionamos "New User".\
\*\
Completamos los datos solicitados para cada usuario.\
\*\
\*\
\*\
Verificamos que aparezcan los usuarios creados.\
\*\
Para configurar la red, ingresamos a la configuración de Ethernet y seleccionamos "Change adapter options".\
\*\
Hacemos clic derecho sobre Ethernet y elegimos "Properties".\
\*\
Seleccionamos "Internet Protocol" y accedemos a sus propiedades.\
\*\
Actualizamos todos los datos internos con los propuestos en la guía.\
\*\
Confirmamos los cambios seleccionando "Aceptar".\
\*\
A partir de este momento, podemos realizar las pruebas de ping y con esto damos por finalizada la configuración.



