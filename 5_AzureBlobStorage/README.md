Nos dirigirnos al portal de [Azure](https://portal.azure.com/#home)

## Paso 1
Para poder trabajar con blob, file, table, etc. lo primero que debemos hacer es crear una cuenta de almacenamiento.
- En la vista principal/home de azure seleccionamos "Cuentas de almacenamiento".

![1](https://user-images.githubusercontent.com/99112892/177248449-4c87124f-7c8f-4142-a73f-a0dadd3e3422.png)

![1 1](https://user-images.githubusercontent.com/99112892/177248495-1f33487d-dda8-429e-8eef-e8ad0a98a66c.png)

### Pestaña:Datos básicos
- Nos aseguramos de que la suscripción es de tipo 'student'.
- Creamos un nuevo grupo de recursos, el cual sería un folder donde vamos a guardar nuestra cuenta de almacenamimento dentro de la nube, lo nombramos como: labs-02.
- Para este ejemplo, nombramos a la aplicación de funciones como "labs02dr2022".
- En la Región para esta ocasion utilizamos East US.  
- Rendimiento: estándar.
- Redundancia: Almacenamiendo con redundancia geográfica(GRS).
- Damos "Revisar y crear".

![1 2](https://user-images.githubusercontent.com/99112892/177248608-e681cdc6-2e73-4ed0-bc14-ce192354ec01.png)

Se crea nuestra cuenta y podre tener acceso a los cuatro servicios principales: blob, queue, table o file storage.
- Seleccionamos "ir al recurso".

![1 3](https://user-images.githubusercontent.com/99112892/177248663-31d0a951-b797-4e2d-bdf6-4ddbd899769b.png)

## Paso 2
Un contenedor nos sirve para guardar las cosas del servicio que usemos, para este caso nos basaremos en un blob.
- En el menu lateral elegimos "Contenedores" y creamos uno seleccionando "Contenedor" en la parte superior.

![1 4](https://user-images.githubusercontent.com/99112892/177248771-e498e60d-d190-4e1c-baae-e6f7e6d98ae5.png)

- Nombre: blob y las otras configuraciones se quedan como estan por default, le damos "crear".

![1 5](https://user-images.githubusercontent.com/99112892/177248821-4970ca88-fe3e-44f0-823e-c9ecfcae8be4.png)

Tenemos el blob listo para cragar cualquier archivo que quieramos(no estructurado).

![1 6](https://user-images.githubusercontent.com/99112892/177248881-6d44dd6d-7bb7-4e47-b438-2935f1809733.png)

![1 7](https://user-images.githubusercontent.com/99112892/177248895-8b986730-8d39-4cd5-9ca4-1974d09e8957.png)


## Paso 3
- Cargaremos una imagen desde nuestra PC.

![1 8](https://user-images.githubusercontent.com/99112892/177248935-3dee5e63-8e4a-498c-af8d-cc10d9c582df.png)

- Obtendremos la siguiente URL, que es donde esta alamacenada la imagen pero si accedemos a ella solo nos servira para descargar la imagen pero no para visualizarla en el navegador.

![1 9](https://user-images.githubusercontent.com/99112892/177248986-f42a8543-022b-424b-9ee6-b71afce2de92.png)

## Paso 4
Para poder visualizar la imagen es necesario "Generar un SAS".
- Seleccionamos "Generar SAS".
- Despues pulsamos en "Generar URL y token de SAS".

![1 10](https://user-images.githubusercontent.com/99112892/177249032-fa42dc2c-ddad-42fc-a2ff-70a4735509c3.png)


- Obtendremos dos URL, pero copiaremos la segunda "URL de SAS de Blob".

![1 11](https://user-images.githubusercontent.com/99112892/177249083-e8aa05f1-bb98-4380-9140-e3aa46931d56.png)

- La pegamos en el navegador y ahora si podremos visualizar la imagen almacenada en el Blob.
Esta imagen ya esta en internet y cualquier persona puede aceeder a verla si tuviera el enlace.

![1 12](https://user-images.githubusercontent.com/99112892/177249124-911b266a-9657-4039-a283-f94b45266a91.png)

Si observamos la URL mas a fondo podemos ver que trae la misma dirección pero tambien la fecha en que se creo y trae un token, el cual es una clave con la que podremos acceder a la imagen.

![1 13](https://user-images.githubusercontent.com/99112892/177249153-457ecd1c-4a6b-485e-be14-1a9d1bb71ad9.png)

# Paso 5
- Eliminamos el blob ya que no lo necesitamos mas.

![1 14](https://user-images.githubusercontent.com/99112892/177249186-80e8f056-0429-4ef4-a432-c407fea166d8.png)

# Paso 6
- Para finalizar nuestro proceso, eliminamos el recurso en nuestro grupo de recursos.

![1 15](https://user-images.githubusercontent.com/99112892/177249227-d1e954ef-79da-49f5-afd7-3bc13cba34b2.png)
