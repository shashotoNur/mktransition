# mktransgif

mktransgif is a Python command-line tool that creates a circular transition GIF between two images. The effect starts from a random point and expands outward, smoothly revealing the "after" image over the "before" image.

## Features

- Generates a circular transition effect between two images

- Automatically resizes mismatched images to the same dimensions

- Able to take images of various formats as input


![Gif of two cats growing up](cats_growing_up.gif "Cats Growing Up")


## Installation

```
pip install Pillow
chmod +x mktransgif
```

## Usage

```
./mktransgif --before BEFORE_IMAGE --after AFTER_IMAGE --output OUTPUT_GIF
```

### Arguments

- `--before` : Path to the "before" image

- `--after`  : Path to the "after" image

- `--output` : Path to save the generated GIF

### Example

```
./mktransgif --before ./sample/cats_year_zero.jpg --after ./sample/cats_year_one.png --output cats_growing_up.gif
```

## License

This project is open-source and available under the [MIT License](LICENCE).

