<h1> Bonsai Example App <img align=right src="https://github.com/tyoverby/bonsai_example/actions/workflows/docker_test.yml/badge.svg" /> </h1>

This repo contains an demo application for
[Bonsai](https://github.com/janestreet/bonsai).

Even more importantly, it also includes reproducable steps for how to build the
dependencies.  The [`./devcontainer`](./.devcontainer) folder contains a
dockerfile which will fully prepare this repo for use, however, you may choose
to just read the file and follow the steps instead of using docker.  That said,
I do recommend using docker alongside the 
["devcontainer" workflow in VS Code](https://code.visualstudio.com/docs/remote/containers).

The project has three main parts, divided up into three subdirectories:
`common`, `client` and `server`.

```
├── .devcontainer 
│   ├── Dockerfile        # A dockerfile for an image that can build this project
│   └── devcontainer.json # VS Code Dev Container support
├── .github/workflows     # Github workflow for continuously building this project
├── scripts               # Handy scripts for building the project
│
├── common                # A shared library which both the client and server link against
├── client                # The web UI, built using Bonsai and Js_of_ocaml
└── server                # The web-server and RPC server
    ├── bin               # The command-line executable for the server
    └── src               # A library containing all the server logic
```

The example itself is a simple chat client, not super interesting, or even very
ideomatic to be perfectly honest.
