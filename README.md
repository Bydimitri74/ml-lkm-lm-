# ml-lkm-lm-

A curated collection of core images that can be used with Bydimitri74's Egg system. Each image is rebuilt
periodically to ensure dependencies are always up-to-date.

Images are hosted on `ghcr.io` and exist under the `games`, `installers`, and `ml-lkm-lm-` spaces. The following logic
is used when determining which space an image will live under:

* `oses` — base images containing core packages to get you started.
* `games` — anything within the `games` folder in the repository. These are images built for running a specific game
or type of game.
* `installers` — anything living within the `installers` directory. These images are used by install scripts for different
Eggs within Bydimitri74, not for actually running a game server. These images are only designed to reduce installation time
and network usage by pre-installing common installation dependencies such as `curl` and `wget`.
* `ml-lkm-lm-` — these are more generic images that allow different types of games or scripts to run. They're generally just
a specific version of software and allow different Eggs within Bydimitri74 to switch out the underlying implementation. An
example of this would be something like Java or Python which are used for running bots, Minecraft servers, etc.

All of these images are available for `linux/amd64` and `linux/arm64` versions, unless otherwise specified, to use
these images on an arm64 system, no modification to them or the tag is needed, they should just work.

## Contributing

When adding a new version to an existing image, such as `java v42`, you'd add it within a child folder of `java`, so
`java/42/Dockerfile` for example. Please also update the correct `.github/workflows` file to ensure that this new version
is tagged correctly.

## Available Images

* [`base oses`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/oses)
  * [`alpine`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/oses/alpine)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:alpine`
  * [`debian`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/oses/debian)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:debian`
* [`games`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/games)
  * [`rust`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/games/rust)
    * `ghcr.io/Bydimitri74/games:rust`
  * [`source`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/games/source)
    * `ghcr.io/Bydimitri74/games:source`
* [`golang`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/go)
  * [`go1.14`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/go/1.14)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:go_1.14`
  * [`go1.15`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/go/1.15)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:go_1.15`
  * [`go1.16`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/go/1.16)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:go_1.16`
  * [`go1.17`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/go/1.17)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:go_1.17`
* [`java`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/java)
  * [`java8`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/java/8)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:java_8`
  * [`java8 - OpenJ9`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/java/8j9)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:java_8j9`
  * [`java11`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/java/11)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:java_11`
  * [`java11 - OpenJ9`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/java/11j9)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:java_11j9`
  * [`java16`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/java/16)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:java_16`
  * [`java16 - OpenJ9`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/java/16j9)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:java_16j9`
  * [`java17`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/java/17)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:java_17`
  * [`java17 - OpenJ9`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/java/17j9)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:java_17j9`
* [`nodejs`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/nodejs)
  * [`node12`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/nodejs/12)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:nodejs_12`
  * [`node14`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/nodejs/14)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:nodejs_14`
  * [`node15`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/nodejs/15)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:nodejs_15`
  * [`node16`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/nodejs/16)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:nodejs_16`
  * [`node17`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/nodejs/17)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:nodejs_17`
* [`python`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/python)
  * [`python3.7`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/python/3.7)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:python_3.7`
  * [`python3.8`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/python/3.8)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:python_3.8`
  * [`python3.9`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/python/3.9)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:python_3.9`
  * [`python3.10`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/python/3.10)
    * `ghcr.io/Bydimitri74/ml-lkm-lm-:python_3.10`

### Installation Images

* [`alpine-install`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/installers/alpine)
  * `ghcr.io/Bydimitri74/installers:alpine`

* [`debian-install`](https://github.com/Bydimitri74/ml-lkm-lm-/tree/main/installers/debian)
  * `ghcr.io/Bydimitri74/installers:debian`
