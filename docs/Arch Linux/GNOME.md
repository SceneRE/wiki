# GNOME

## Ver todas las ventanas de cada aplicación con Alt-Tab en GNOME 40+

En Settings > Keyboard ir a Shorcuts

![](/assets/images/gnome-01.png)

Buscar "switch windows" y asignar Alt+Tab

![](/assets/images/gnome-02.png)

## Los iconos de las aplicaciones desaparecieron

!!! danger
    
    Vera el siguiente comando en Internet, **NUNCA** lo ejecute a menos que sepa lo que hace, puede llevarlo a un problema aun mayor.

    ```gdk-pixbuf-query-loaders --update-cache```

Reinstale los siguientes paquetes relacionados con los iconos, en el orden que aparecen:

```
yay -S adwaita-icon-theme
yay -S gnome-icon-theme
yay -S glib2
yay -S librsvg
yay -S gdk-pixbuf2
```

Luego reinicie la shell con ```Alt+F2 > r > enter```

Si no funciona, pruebe reinstalar solo estos paquetes en el siguiente orden:

```
yay -S gdk-pixbuf2
yay -S librsvg
```

También es posible que necesite reiniciar Linux si persiste el problema.