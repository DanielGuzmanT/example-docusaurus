# Docusaurus Example
Este es un proyecto creado para el taller de Git organizado por la AAII 🚀.

# Despliegue

## GitLab
1. colocar los datos necesarios en el archivo `.gitlab.env` que se usarán para desplegar la pag web
```
URL=https://<gitlab-username>.gitlab.io
BASE_URL=/
PROJECT_NAME=<project-name>
ORGANIZATION_NAME=<gitlab-user>
```

2. cambiar el nombre del archivo `.gitlab.env` por `.env`

3. en el archibo `.gitlab-ci.yml`, cambiar el último comando del `script` colocando el nombre correcto del proyecto:
```yaml
image: node:lts

pages:
  script:
    - cd website
    - yarn install
    - yarn build
    - mv ./build/<project-name> ../public
  artifacts:
    paths:
      - public
  only:
    - master
```

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

