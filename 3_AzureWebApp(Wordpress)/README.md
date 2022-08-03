# AZ900-WebApp(Wordpress)

"App Service" es un servicio que se utiliza para las aplicaciones de grado empresarial este servivcio es un servicio web.

Guía para crear una Web App dentro de Azure utilizando wordpress.

Lo primero que debemo hacer, es dirigirnos al portal de Azure.


## Paso 1
En en la vista de Home nos posicionamos en el buscador que se enceuntra en la parte superior y escribimos "wordpress" y seleccionamos la primer opción.

![1](https://user-images.githubusercontent.com/99112892/182535831-05a8b8f2-63b1-47d8-81d8-e9bd8bb5cd46.png)

## Paso 2
### Pestaña:Datos básicos
- Nos aseguramos de que la suscripción es de tipo 'student'.
- Creamos un nuevo grupo de recursos, el cual sería un folder donde vamos a guardar nuestra aplicación web dentro de la nube, lo nombramos como: lab03-dr.
- En la Región para esta ocasion utilizamos East US.
- Le damos un nombre a nuestra aplicación web, en este caso la nombro: lab003--dr.
- Para el sistema operativo seleccionamos "Linux" con su plan de hospedaje Básico.

![2](https://user-images.githubusercontent.com/99112892/182535900-a2846bf0-067e-4676-b0d8-368716fa8809.png)

- En el nombre de uruario del administrador nos arroja uno automaticamente pero es mejor cambiarlo por uno que recordemos.
- Ponemos una contraseña y la confirmamos.
- Le damos click en el boton "Avanzados" para acceder a esa sección.

![3](https://user-images.githubusercontent.com/99112892/182536064-95bd8714-2b2e-47fe-b65d-02197d9d4125.png)

### Pestaña:Avanzados(Advanced)
- Para el idioma del sitio ocupamos English (United States).
- La distribución de contenido la deshabilitamos.
- Le damos click en el boton "Etiquetas" para acceder a esa sección.

![4](https://user-images.githubusercontent.com/99112892/182536332-104544e5-30ff-4305-94f8-2e8e3db47ff6.png)

### Pestaña:Etiquetas(Tags)
Las etiquetas nos sirven para cuando hay muchas personas trabajando dentro de una organización,es importante saber quien esta subiendo que cambios. 
- En el campo nombre es muy usual poner: CreatedBy y para el campo valor ponemos por quien fue creado.
- Agregamos otra etiqueta con Nombre:Area y Valor:Rivan.
- Finalizamos con una ultima Nombre:Ciclo y Valor:7maEd.
- Le damos click en el boton "Revisar y crear" y despues de que se analiza y aprueba la implementación le damos en crear.

![5](https://user-images.githubusercontent.com/99112892/182536414-223dec6a-8092-464f-8fbc-054ef04a75e8.png)

- Esperaremos la implementación, puede tardar alrededor de 5 minutos.

![6](https://user-images.githubusercontent.com/99112892/182536556-9c44cf2a-7d2b-49b7-99ce-a2d18f894fb5.png)

- Lista la implementación, hacemos click en "ir al recurso".

![7](https://user-images.githubusercontent.com/99112892/182536613-39e2c569-d006-4d73-9109-41e22e3be7d5.png)

## Paso 3
- En la información esencial de nuestro "lab03--dr" vamos a dirigirnos en donde dice URL,esto nos instalara de forma automatica Wordpres, es decir nos va instalar dentro de nuestra aplicación web un sistema que nos permita poder trabajar con las aplicaciones Web.

![8](https://user-images.githubusercontent.com/99112892/182536648-eb42f2bf-dc05-4688-ae06-41ca7031af6b.png)

- Despues de la intalación exitosa, nos manda a esta página.

![9](https://user-images.githubusercontent.com/99112892/182536765-d49fe973-4ce2-447d-b483-baa84f21fc96.png)

## Paso 4
- Nos dirigimos a la dirección de la página y nos posicionamos al final de la misma, donde agregaremos "/wp-admin" , esto es para que nos mande al login de wordpress.

![10](https://user-images.githubusercontent.com/99112892/182536826-4010688e-9bfb-41a5-a670-049b9e873c64.png)

## Paso 5
- Nos pedira usuario y contraseña, ingresaremos los datos que utilizamos al crear nuestro "lab03--dr".

![11](https://user-images.githubusercontent.com/99112892/182536925-b6a4bac9-6bbc-481a-a3be-6bd91333247b.png)

- Tendremos acceso a la siguiente interfaz.

![12](https://user-images.githubusercontent.com/99112892/182537012-5fe1e790-dadd-480c-a055-c2bdd69f4ca8.png)

## Paso 6
- En la pestaña "Appearance" podemos elegir algún tema para nuestra web app.

![13](https://user-images.githubusercontent.com/99112892/182537055-94bcf729-711e-40bc-9729-e36a1e0178e8.png)

- Lo instalamos.

![14](https://user-images.githubusercontent.com/99112892/182537164-82664b22-f9be-415f-9a20-7a2552121017.png)

- Lo activamos y ahora solo tenemos que editarlo a nuestro gusto para posteriormente publicarlo.

![15](https://user-images.githubusercontent.com/99112892/182538634-54f71f7d-be10-4114-a9ac-7ba82c83f9eb.png)

## Paso 7
- Para asegurarnos de que los cambios se han efectuado, solo tenemos que volver a ingresar a la URL de la implementación y lo verificamos.

![16](https://user-images.githubusercontent.com/99112892/182538705-d80fbb80-3e57-433d-80f8-0a800d184742.png)
