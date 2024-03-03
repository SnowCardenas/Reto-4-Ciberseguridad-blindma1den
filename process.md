```
hydra -l admin -P rockyou.txt 127.0.0.1 ssh -s 2222 -t 4
```
```-l ```
(parametro para especificar el "login" o usuario en individual, en este caso `admin`)

```admin``` 
(valor del parametro -l como usuario o login)

```-P ```
(parametro en mayúscula que especifica que tomará una lista de palabras o de cadenas de texto, en este caso `rockyou.txt`)

```rockyou.txt``` 
(famoso documento de texto que contiene mas de 12 millones de contraseñas y cadenas de texto que se usan comunmente)

```IP 127.0.0.1 ```
(IP VICTIMA)
(Local Host, https://hipertextual.com/2015/01/que-es-la-ip-127-0-0-1)
(Es la direccion IP de localhost, es decir la de tu casa, tu host, el equipo local.)

```ssh```
(parametro para especificar el protocolo victima - servicio ssh)

```-s 2222```
(parametro junto a su valor donde se escribe un puerto en especifico, en este caso 2222)

```-t 4```
(parametro que establece el numero de tareas paralelas (hilos) que se ejecutarán)

