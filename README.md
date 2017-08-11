<img src="fugu.png" height="160">

# What is fugu?

 * fugu is a convenience wrapper around docker commands
 * fugu loads config from a fugu.yml file and 
   merges these arguments with command line flags.

__Example__

```yml
# fugu.yml (maybe stored next to Dockerfile)
image:  ubuntu
name:   my-ubuntu
publish:
  - 8080:80
```

```bash
$ fugu run --detach # runs ...
docker run --detach --name=my-ubuntu --publish=8080:80 ubuntu
```

Fugu commands include: ``build``, ``run``, ``exec``, ``destroy``, 
``push``, ``pull``, ``images``.

# Installation

```bash
# Mac OS X
curl -L https://github.com/mattes/fugu/releases/download/v1.1.1/fugu.v1.1.1.darwin.x86_64.tar.gz | tar xvz
mv fugu.v1.1.1.darwin.x86_64 /usr/local/bin/fugu
chmod +x /usr/local/bin/fugu

# Linux
curl -L https://github.com/mattes/fugu/releases/download/v1.1.1/fugu.v1.1.1.linux.x86_64.tar.gz | tar xvz
mv fugu.v1.1.1.linux.x86_64 /usr/local/bin/fugu
chmod +x /usr/local/bin/fugu
```


## How is this different from docker-compose/ fig?

While [aciklovir allvarliga biverkningar](http://www.herpesvirus.se/aciklovir/) (originated from ``fig``) 
focuses on the definition and orchestration of complex application environments, 
fugu focuses on one single docker container/ docker image.

## Changelog

Find the changelog and breaking changes here:
https://github.com/mattes/fugu/releases

