### Creación de la Máquina Virtual de Windows

### Máquina sin interfaz

Podemos seleccionar el teclado en español Colombia.

![Captura5](https://github.com/user-attachments/assets/09666b1a-a346-428e-801a-67a577c4ad2b)

En este caso, como se quiere instalar sin interfaz gráfica, seleccionamos la versión Standard.

![imagen](https://github.com/user-attachments/assets/da526663-3a63-4d8d-9169-3b0ce9e4f3b3)

Aceptamos los términos.

![imagen](https://github.com/user-attachments/assets/beb2b444-5014-46a0-b992-fe7cb0feb85e)

Elegimos la instalación personalizada.

![Captura28](https://github.com/user-attachments/assets/3bfaa0ff-3db6-4a55-b7bc-d87f10b517b5)

Seleccionamos el disco recién creado.

![Captura29](https://github.com/user-attachments/assets/55943cf2-80b1-41fb-858c-a7fa3b6b6e4c)

Esperamos un rato a que instale.

![imagen](https://github.com/user-attachments/assets/d31c719c-12b7-4dce-bc0a-7d3ffde4d45a)

Seleccionamos "OK" para asignarle una contraseña.

![imagen](https://github.com/user-attachments/assets/94c9f194-e41f-4ae5-8e2e-67cd85882d41)

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

Escribimos los datos dados por el laboratorio en nuestro caso Adrress: 10.2.78.51 Mask: 255.255.0.0 Gateway: 10.2.65.1.

![Captura45](https://github.com/user-attachments/assets/9553d923-3c0d-471a-92aa-fdaf1818915c)

Después de presionar ENTER, ingresamos nuevamente al menú seleccionando la opción 8.

![Captura44](https://github.com/user-attachments/assets/a1605596-6157-4dba-bba5-c2eb086635fe)

Accedemos a la configuración de DNS.

![Captura46](https://github.com/user-attachments/assets/1cdfb86b-dd2d-4253-bd28-5c43fc1c1e59)

Ingresamos el DNS proporcionado por la guía "10.2.65.1".

![Captura47](https://github.com/user-attachments/assets/dc8b12dd-ff24-4455-aa48-2d8bfbad8d54)

Salimos de la configuración eligiendo la opción 15.

![Captura48](https://github.com/user-attachments/assets/5beb8399-a094-4b2e-8ed5-45b14617eb7f)

Iniciamos las pruebas de ping, empezando por "8.8.8.8".

![imagen](https://github.com/user-attachments/assets/6beeade2-2de1-4ac5-b1be-f7ab76d15fa0)

### Máquina con interfaz

Realizamos los primeros pasos de la misma manera que en la anterior.
En este punto, a diferencia de la máquina anterior, seleccionamos "Standard (Desktop Experience)".

![Captura27](https://github.com/user-attachments/assets/5c2d40a7-b1ba-42cb-a5e4-189606c85106)

Seleccionamos la instalación "Custom".

![Captura28](https://github.com/user-attachments/assets/4542a200-e900-4c12-b5c7-fc042e1bd91a)

Elegimos el disco recién creado.

![Captura29](https://github.com/user-attachments/assets/58971fce-da18-4adf-b26f-af0df4e92918)

Esperamos a que termine la instalación.

![Captura30](https://github.com/user-attachments/assets/7369b47c-c920-4255-ab1a-c24a41329006)

Iniciamos la configuración asignando una contraseña para el perfil de Administrador "Root123".

![imagen](https://github.com/user-attachments/assets/d2b1d261-0b68-4e29-84e5-19f6c32a618d)

Después de acceder, nos encontramos en esto.

![imagen](https://github.com/user-attachments/assets/d7543964-1fe7-4b52-841a-3c5516a35e13)

Para crear los demás usuarios, entramos en cmd e ingresamos los siguientes comandos para agregar a cada usuario a un rol distinto.

![imagen](https://github.com/user-attachments/assets/abb00f60-0f6c-4634-a925-e1d6eac4e25b)

![imagen](https://github.com/user-attachments/assets/bccbf7ee-013d-4bc8-82c3-7424178c9f7c)

Para configurar la red, ingresamos a la configuración de Ethernet y seleccionamos "Change adapter options".

![imagen](https://github.com/user-attachments/assets/0484a2a9-b2ce-48ac-9505-ccddb5303f35)

Hacemos clic derecho sobre Ethernet y elegimos "Properties".

![imagen](https://github.com/user-attachments/assets/4797121f-ff47-4a35-92fb-be1b6ed7f0ac)

Seleccionamos "Internet Protocol" y accedemos a sus propiedades.

![imagen](https://github.com/user-attachments/assets/4217b6ef-1914-4e31-b75d-361633c42e3e)

Actualizamos todos los datos internos con los propuestos en la guía.

![imagen](https://github.com/user-attachments/assets/38fc1b51-b22a-4d61-8bc8-d7eec43c6fad)

Confirmamos los cambios seleccionando "Aceptar".

![imagen](https://github.com/user-attachments/assets/a3785dba-e256-470e-a08f-f6ddf960f7c5)

A partir de este momento, podemos realizar las pruebas de ping y con esto damos por finalizada la configuración.



