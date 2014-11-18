# Easily test on 5 distros using Docker

###Setup environment

```
$ git clone https://github.com/jdolitsky/dockerspaniel-demo.git
$ cd dockerspaniel-demo
$ npm install
$ export PATH=./bin:$PATH
```

### Create Dockerfiles

Using base images listed in *base_images.txt*, create custom Dockerfiles using dockerspaniel.

```
$ create_dockerfiles
```

### Build Docker images

Build Docker images using the Dockerfiles created with `create_dockerfiles`.

```
$ build_images
```

### Test on each platform

Clone an app (dockerspaniel), then mount and build inside each of our custom images.

```
$ run_tests
```

The console output of each build can be accessed at *build/$DISTRO_$RELEASE/build.log* (e.g. *build/debian_wheezy/build.log*).
