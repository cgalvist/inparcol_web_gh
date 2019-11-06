# Comandos útiles

## Convertir muchas imágenes PNG a JPG

Instalar Image Magick:

```shell
sudo apt-get update
sudo apt-get install imagemagick
```

Y ejecutar la siguiente orden:

```shell
mogrify -format jpg *.png
```

## Renombrar muchas imágenes JPG a una lista numerada

```shell
n=1; for f in *.jpg; do mv "$f" "$((n++)).jpg"; done
```