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

## Comprimir imágenes JPG

```shell
mogrify -quality 100 -resize 800x600 *.jpg
```

El comando anterior comprime todas las imágenes JPG sin perder calidad de color, pero reduciendo su resolución.
La resolución `800x600` no se tendrá en cuenta de manera literal, ya que se preservará la relación de aspecto. Dependiendo de la proporción de la imágen se reducirá su ancho o alto.