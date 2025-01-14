<p align="center"><img src="https://user-images.githubusercontent.com/1092882/86526373-07f1d700-beb1-11ea-815b-934d2ea67e0a.png" alt="docker gopher" width="256px"/></p>

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

# Go Dockerfile v0.1.6

[Dockerfiles](https://docs.docker.com/engine/reference/builder/) to build [Docker images](https://docs.docker.com/engine/docker-overview/#docker-objects) for your [Go](https://go.dev) app. It makes use of Docker's [multi-stage build feature](https://docs.docker.com/develop/develop-images/multistage-build/) to create the Go application binary, and then attach it to a minimal base image. The Go version used is `1.22`, though it should work for most Go versions (not tested). You'll have to tweak the Dockerfile to `COPY` any static files required by the application, to be copied to the final image.

There are 4 Dockerfiles provided

1. [Debian](https://www.debian.org/) slim based
2. [Alpine](https://alpinelinux.org/) based
3. [BusyBox](https://www.busybox.net/) based
4. [Scratch](https://hub.docker.com/_/scratch) (no base OS layer)

It's important that you understand [Go build flags](https://pkg.go.dev/cmd/go#hdr-Compile_packages_and_dependencies) to build a functioning binary for your application. Not all apps will work with build configuration provided in the Dockerfiles.

## How to build the example

```bash
$ docker build -t webgo-helloworld-alpine -f Dockerfile-alpine ./example

$ docker build -t webgo-helloworld-debian -f Dockerfile-debian ./example

$ docker build -t webgo-helloworld-busybox -f Dockerfile-busybox ./example

$ docker build -t webgo-helloworld-scratch -f Dockerfile-scratch ./example
```

## How to run?

```bash
$ docker run -p 8080:8080 --rm -ti webgo-helloworld-alpine
$ docker run -p 8080:8080 --rm -ti webgo-helloworld-debian
$ docker run -p 8080:8080 --rm -ti webgo-helloworld-busybox
$ docker run -p 8080:8080 --rm -ti webgo-helloworld-scratch
```

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
