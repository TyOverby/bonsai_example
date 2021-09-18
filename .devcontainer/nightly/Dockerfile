FROM ocaml/opam:alpine-ocaml-4.12

USER root
RUN sed -i 's-/home/opam:/sbin/nologin-/home/opam:/bin/bash-' /etc/passwd
RUN apk add git inotify-tools openssh openssl-dev libffi-dev zlib-dev pcre neovim gmp-dev pcre-dev

USER opam

RUN opam repo add janestreet-bleeding https://ocaml.janestreet.com/opam-repository
RUN opam repo add janestreet-bleeding-external https://github.com/janestreet/opam-repository.git#external-packages
RUN opam update

RUN opam install dune base merlin ocamlformat ppx_jane ocaml-lsp-server bonsai

RUN mkdir -p ~/.cache/nvim