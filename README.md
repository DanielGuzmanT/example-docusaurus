# Docusaurus Example
Este es un proyecto creado para el taller de Git organizado por la AAII 🚀.

# Despliegue

## GitHub

1. colocar los datos necesarios en el archivo `.github.env` que se usarán para desplegar la pag web

2. cambiar el nombre del archivo `.github.env` por `.env`

3. ejecutar el siguiente comando:
```bash
GIT_USER=<git-username> USER_SSH=false yarn run publish-gh-pages
```

__Observaciones:__
- Si se està usando `ssh` para pushear a alguno de los repositorios, cambiar `USER_SSH`
a `true`.

