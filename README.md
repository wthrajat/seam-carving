# Seam Carving  ![OpenCV](https://img.shields.io/static/v1?style=for-the-badge&message=OpenCV&color=5C3EE8&logo=OpenCV&logoColor=FFFFFF&label=) ![C++](https://img.shields.io/static/v1?style=for-the-badge&message=C%2B%2B&color=00599C&logo=C%2B%2B&logoColor=FFFFFF&label=) ![CMake](https://img.shields.io/static/v1?style=for-the-badge&message=CMake&color=064F8C&logo=CMake&logoColor=FFFFFF&label=) [![Badge](https://img.shields.io/badge/Seam-Carving-pink.svg)](https://shields.io/) [![GitHub license](https://img.shields.io/github/license/Naereen/StrapDown.js.svg)](https://github.com/Naereen/StrapDown.js/blob/master/LICENSE)

[Seam carving](https://en.wikipedia.org/wiki/Seam_carving) (or liquid rescaling) is an algorithm for content-aware image resizing, developed by Mitsubishi Electric Research Laboratories (MERL). It functions by establishing a number of seams (paths of least importance) in an image and automatically removes seams to reduce image size or inserts seams to extend it.

## Dependencies

Make sure to install the following minimal dependencies to avoid build errors:
- [Glew](https://archlinux.org/packages/extra/x86_64/glew/)
- [lib32-glew](https://archlinux.org/packages/multilib/x86_64/lib32-glew/)
- [CMake](https://cmake.org/download/)
- [OpenCV](https://opencv.org/releases/)

## Build

```sh
git clone https://github.com/wthrajat/seam-carving.git
cd seam-carving && mkdir build && cd build && cmake .. && make
```
After compilation, this will build an executable `"seam_carving"` at `./build/app/`:
```sh
./build/app/seam_carving
```

## Usage

```sh
./build/app/seam_carving <input_image> <direction> <number of seams> <mode> <x> <y> <w> <h>

# OR

./build/app/seam_carving <input_image> <direction> <number of seams>

```

## Format of arguments
```rust
<direction> : 'h'(horizontally) OR 'v'(vertically)

<mode> : 'r' OR 'p'
'r' for removal
'p' for protection

<x> <y> <w> <h> : Specifies the region of interest

```

## Examples

