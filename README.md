# Reto #4 de Ciberseguridad - SSH Vulnerable a Fuerza Bruta

¡Bienvenido al reto #4 de Ciberseguridad! En este desafío estaremos desplegando un contenedor Docker que tiene el servicio SSH vulnerable a fuerza bruta.

## ¿Qué es Docker?

Docker es una plataforma de código abierto que facilita la creación, implementación y ejecución de aplicaciones en contenedores. Los contenedores son unidades de software que incluyen todo lo necesario para que una aplicación se ejecute, incluidas las bibliotecas, dependencias y configuraciones.

## ¿Qué es SSH?

SSH (Secure Shell) es un protocolo de red que permite la comunicación segura y cifrada entre dos dispositivos, típicamente un cliente y un servidor. Se utiliza comúnmente para acceder de forma remota a sistemas Unix y Linux, proporcionando una interfaz de línea de comandos segura.

## ¿Qué es Fuerza Bruta?

La fuerza bruta es un método utilizado en ciberseguridad para descifrar contraseñas o encontrar claves de cifrado probando todas las combinaciones posibles hasta encontrar la correcta. Este método puede ser muy efectivo pero también es intensivo en recursos y puede llevar mucho tiempo. Para este reto, utilizaremos dos herramientas de fuerza bruta comunes: Hydra y Medusa.

## Preparación

Antes de comenzar, asegúrate de tener Docker instalado en tu sistema. Si no lo tienes instalado, puedes hacerlo en sistemas basados en Debian/Ubuntu utilizando el siguiente comando:

```
sudo apt install docker.io
```

Una vez instalado Docker, inicia el demonio de Docker con el siguiente comando:

```
sudo service docker start
```

## Despliegue del Contenedor

1. Crea una carpeta en tu sistema y descarga el archivo `ssh.env`. Mueve el archivo a la carpeta que acabas de crear.

2. Ejecuta el siguiente comando para desplegar el contenedor Docker con el servicio SSH vulnerable:

```bash
docker run -d \
  --name=openssh-server \
  --hostname=blindma1den-ssh \
  --env-file ssh.env \
  -p 2222:2222 \
  --restart unless-stopped \
  lscr.io/linuxserver/openssh-server:latest
```

## Desafío

Una vez desplegado el contenedor, el servicio SSH estará disponible en el puerto 2222. El usuario para el SSH es "admin". Utilizando una herramienta de fuerza bruta como Hydra o Medusa y el diccionario "rockyou" (que normalmente se encuentra en `/usr/share/wordlists/`), tu objetivo es encontrar la contraseña para el usuario "admin".

¡Es hora de hackear!

---

La solucion esta descrita en el pdf "Reto 4 ciberseguridad.pdf"
