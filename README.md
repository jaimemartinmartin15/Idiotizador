# Idiotizador

Application that listens to the microphone and plays it back with a delay. Deployed to <https://jaimeelingeniero.es/idiotizador>

[![Build And Deploy](https://github.com/jaimemartinmartin15/Idiotizador/actions/workflows/build-and-publish.yml/badge.svg)](https://github.com/jaimemartinmartin15/Idiotizador/actions/workflows/build-and-publish.yml)

## Development

**Clone** the repository:

```text
git clone https://github.com/jaimemartinmartin15/Idiotizador.git
```

**Start** the server:

```text
live-server .
```

## Deploy

After doing the changes in your branch, update the [CHANGELOG.md](./CHANGELOG.md) file.

Then merge the changes in `main` branch and create a tag with the same version than in the [CHANGELOG.md](./CHANGELOG.md).

When pushing the tag to the remote, it will trigger the workflow **build-and-publish.yml** automatically to deploy it.

## Workflows

### build-and-publish.yml

Optimices the index.html and deploys the application to the server.

Basically, it copies the optimized files and puts them in `idiotizador/` folder in the server.
