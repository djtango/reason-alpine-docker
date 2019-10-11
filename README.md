# Reason Alpine Docker
Build a docker image that comes with the BuckleScript/Reason toolchain on
Alpine Linux.  

Note I wrote this entirely for personal use: having containerized Node and
Python environment on a minimal Linux felt nice for my sanity - I would not
recommend this for
production usage (though, equally it is not particularly complex...)  

What it does:
* Start from the [Node Alpine](https://hub.docker.com/_/node/) image as base
* Install Python by copying same steps from the [Node
  Python](https://github.com/docker-library/python/blob/c3233a936f58bee7c6899d3e381f23ed12cfc7a8/3.7/alpine3.10/Dockerfile)
  image as [Ninja](https://github.com/scemama/ninja_ocaml) requires Python.
* Install `bs-platform@5.2.0` note that at the time of writing, `5.0.6` was the
  latest `bs-platform` release but only `5.2.x` [onwards is compatible with
  Alpine](https://github.com/BuckleScript/bucklescript/issues/3666)
