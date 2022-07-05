# qiot-ubi-multiarch-builder-demo
A plain copy of the getting-started project from the Quarkus quickstarts to demonstrate how to compile aarch64 native images on x86-based cpu architectures.

To build the container image for aarch64 native platforms on an x86 cpu architecture run the following commands:

```
docker run --rm --privileged multiarch/qemu-user-static:register --reset
```
```
docker build -t quarkus-quickstart-getting-started:2.9.2-aarch64 -f src/main/docker/Dockerfile.native-aarch64 .
```