# Cross

Utilities for cross-compiling in a container.

## Usage

```sh
docker run -v /some/c/src:/src cross arm-unknown-linux-musleabihf-g++ -some -options /src/your/src.cpp -o /src/is-useful-mounted
```

Requires sysroots, i.e. from `e-dant/sysroots/cross.py`.
The sysroots should be in `$PWD/sysroots` during docker build-time.

## Available Targets

- `aarch64-unknown-linux-gnu`
- `armv7-unknown-linux-gnueabihf`
- `arm-unknown-linux-gnueabihf`
- `x86_64-unknown-linux-gnu`
- `i686-unknown-linux-gnu`
- `aarch64-unknown-linux-musl`
- `armv7-unknown-linux-musleabihf`
- `arm-unknown-linux-musleabihf`
- `x86_64-unknown-linux-musl`
- `i686-unknown-linux-musl`
