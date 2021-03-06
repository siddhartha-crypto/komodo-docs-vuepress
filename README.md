# Readme

Built using [Vuepress](https://vuepress.vuejs.org/)

## Setup:

> Prerequisites: nodejs and yarn.

* Clone the repository
* `cd` into the directory `cd komodo-docs-vuepress/`

Install Vuepress globally

```shell
yarn global add vuepress
```

Or install as a local dependency

```shell
yarn add -D vuepress
```

Install packages

```shell
yarn install
```

## Start Editing

```shell
yarn docs:dev
```

HTML output is displayed at http://localhost:8080

>Edit the markdown files in the directory `docs`

If the changes are not reflected right away, refresh the page.

Exit the dev mode by doing `CTRL + C` in the same terminal `yarn docs:dev` has been done. 

Issuing the build command while the above dev command is active might cause the build to fail with errors.

## Build

```shell
yarn docs:build
```

The html files are available in `komodo-docs-vuepress/docs/.vuepress/dist/`

## Deploy

To deploy to gh-pages at `https://<USERNAME>.github.io/<REPO>`

```shell
./deploy.sh
```

The above script uses your `git <USERNAME>` from the Global git configuration.

## Using Docker:

You can use Docker to reliably produce a developer environment that won't conflict with any of your existing projects.

> Prerequisites: Install Docker and Docker Compose on your system

* To start developing, simply issue `docker-compose up` in a terminal to launch the container
* Then do `docker exec -ti komodo_docs /bin/sh` in another terminal to access a terminal inside the container. Now simply follow the instructions detailed in the above `Start Editing` , `Build` sections.
* To exit from the terminal from the container use the `exit` command.
* Use `CTRL + C` in the terminal `docker-compose up` has been done to stop the container.
* To deploy using docker, use the command `./deploy_docker.sh`

* When used for the first time, Docker might take some time to download the required data and build an image. Subsequent usage will be faster.

