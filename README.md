# Bitácora Técnica IV. Laboratorio de Teletransportación Digital (SSH y RDP)
## Tarea 1: Despliegue de la Infraestructura
He creado una carpeta llamada _SI_Bitacora4_SantiagoGonzalez_, en ella he creado el archivo _docker-compose.yml_ como se indica en la práctica.

Con el _Docker Desktop_ abierto, he ejecutado en la terminal el comando _docker-compose up -d_.
![docker-compose up -d](imagenes/docker-compose_up_-d.png)

Luego he verificado que los contenedores están corriendo con _docker ps_ y dentro de la aplicación _Docker Desktop_.

![docker ps](imagenes/docker_ps.png)
![docker desktop](imagenes/docker_desktop.png)


## 3.1. SSH: Forjando la Llave Maestra
### Paso A (Conexión Inicial)
Para conectarme al contenedor he usado el comando _ssh alumno@localhost -p 2222_ con contraseña _sistemas_informaticos_.
![ssh alumno@localhost -p 2222](<imagenes/ssh alumno@localhost -p 2222.png>)

### Paso B (Generación de Identidad)
Luego he generado un par de llaves con el comando _ssh-keygen -t ed25519 -C "mi_correo@ejemplo.com"_
![ssh-keygen -t ed25519 -C](<imagenes/ssh-keygen -t ed25519 -C.png>)

### Paso C (Transferencia)
Para copiar mi clave pública al servidor he usado el comando _ssh-copy-id -p 2222 alumno@localhost_
![ssh-copy-id -p 2222 alumno@localhost](<imagenes/ssh-copy-id -p 2222 alumno@localhost.png>)


## 3.2. RDP: El Escritorio en tu Navegador
Me he intentado conectar por Escritorio remoto con la aplicación _MSTSC_ de Windows por la dirección _localhost:3389_.
![MSTSC](imagenes/MSTSC.png)
Pero me salía un error de que el equipo no podía conectarse ya que hay una sesion de consola en curso.
![MSTSC Error](<imagenes/MSTSC Error.png>)

Por ello me fui a la dirección _http://localhost:3000_
![localhost 3000](<imagenes/localhost 3000.png>)