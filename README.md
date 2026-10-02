# tobyte

Convert files into C/C++ header files containing raw bytes.

## Use

Drag one or more files onto `tobyte.exe`.

Example:

```bat
tobyte.exe image.png
```

This creates `image.h` next to `image.png`.

The generated header contains:

```c
static const unsigned char image_png[] = { ... };
static const unsigned long long image_png_size = ...ULL;
static const char image_png_name[] = "image.png";
```

## Build

```bat
cargo build --release
```

The executable is generated here:

```text
target\release\tobyte.exe
```
