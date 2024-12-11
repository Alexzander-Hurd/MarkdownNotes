# Markdown Notes SPA

This is a solution for https://roadmap.sh/projects/markdown-note-taking-app written in ASP.NET Core for the backend API and React for the front end.

## Prerequisites

Building a docker stack requires docker with compose to be installed,
Building from source requires dotnet-sdk 8.0 or higher (if you are using a different framework than 8 you will need to specify --framework 8.0 at the build step) and nodeJS version LTS-Jod (22.11.0) or higher 

## Build Steps

To build the application into a docker compose stack run the following:
```sh
$ ./docker_build.sh
```
This will create a docker compose stack with it's own network running the front and back end with nginx as a reverse proxy

To build without docker:
```sh
# dotnet
$ cd api
$ dotnet build -c Release -o build
# This produces a DLL of the API

# Vue
$ cd vue
$ yarn install
$ yarn run build
```

To run without building

```sh
Backend
$ cd api && dotnet run

Frontend
$ cd vue/frontend && yarn serve
```