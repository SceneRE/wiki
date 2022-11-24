# Arch Linux

## Desbloquear el usuario de Linux después de demasiados intentos de inicio de sesión fallidos

Para ver la cuenta de intentos fallidos puede ejecutar el comando:

`$ faillock --user usuario`

Verá algo como:

```
When            Type     Source     Valid
Timestamp 1     TTY      /dev/tty1  V
Timestamp 2     TTY      /dev/tty1  V
Timestamp 3     TTY      /dev/tty1  V
```

Luego debe iniciar sesión como un usuario con capacidades de sudo y reiniciar el conteo del usuario:

```
$ su root
# faillock --user usuario --reset
```