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

### Local testing deployment

To test the deployment locally, follow same instructions than in the workflow:

- Add `.npmrc` file
- Install dependencies.

  ```bash
  npm install @jaimemartinmartin15/jei-devkit-angular-builders@5.2.1 html-minifier-terser --save-dev
  ```

  The angular cli is supposed to be already installed globally.

  `package.json` and `package-lock.json` are not commit.

- Create the dist folder:

  ```bash
  mkdir -p dist
  npx html-minifier-terser index.html -o dist/index.html --collapse-whitespace --remove-comments --minify-css true --minify-js true
  cp -r favicons dist/favicons/
  ```

- Finally run `ng deploy`.

## Workflows

### build-and-publish.yml

Optimices the index.html and deploys the application to the server.
