Para la ejucion de la aplicacio primero hemos de añadir las variables de entorno en el archivo
.env y guardarlo

Usa esta plantilla para crear la DB ejemplo de .env

	MYSQL_HOST=db
	MYSQL_USER=usuario
	MYSQL_PASSWORD=secret
	MYSQL_DATABASE=empresa
	MYSQL_ROOT_PASSWORD=rootsecret

Lo siguiente es el archivo Dokerfile, este almacena instruciones previas a la ejecucion
del conenedor instalando dependencias neccesarias para la ejecuccion de la aplicaccion.

Comandos utiles: 
		(Creacion volumenes) >> docker compose up -d --builddocker
		(Deshabilitar) >> docker compose down -v
		(Ver estado) >> docker ps
		
Ahora para ejecutar el composer.yaml debemos realizar este listado de comandos.

Guia de uso:
    1.- Importar la imagen >>> docker pull p0k0io/dockernicoejercicio:v1
    2.- Crear el .env con tus propias credenciales
    3.- Iniciar el contenedor con el comando >>> docker run --env-file .env -p 8080:80 p0k0io/dockernicoejercicio:v1
    4.- Asegurate de que el .env esta en la carpeta actual desde la que se va a ejecutar el comando anterior de otra manera no cargara
    


