# mktransition

**mktransition** is a Python command-line tool that creates a circular transition webp between two images.  
The effect starts from a random point and expands outward, smoothly revealing the "after" image over the "before" image.

## Features

- Creates a smooth circular transition effect between two images  
- Accepts common image formats as input  
- Automatically resizes mismatched images to match dimensions  
- Configurable transition speed, duration, curve, quality, and looping  

<br>

![Gif of two cats growing up](cats_growing_up.webp "Cats Growing Up")

## Installation

```bash
pip install Pillow
chmod +x mktransition
````

## Usage

```bash
./mktransition --before BEFORE_IMAGE --after AFTER_IMAGE --output OUTPUT_GIF [options]
```

### Arguments

* `--before` : Path to the "before" image (required)
* `--after`  : Path to the "after" image (required)
* `--output` : Path to save the generated GIF (required)
* `--steps` : Number of frames in the transition (default: 60)
* `--frame-duration` : Duration of each frame in ms (default: 50)
* `--pause-duration` : Time period to show the before and after images in ms (default: 1500)
* `--power` : Acceleration of transition curve (default: 5)
* `--max-size` : Maximum GIF resolution (default: 1024)
* `--loop` : Number of times to loop the GIF, 0 = infinite (default: 0)
* `--quality` : GIF quality (default: 80)

### Example

```bash
./mktransition \
  --before ./sample/cats_year_zero.jpg \
  --after ./sample/cats_year_one.png \
  --output cats_growing_up.gif \
  --steps 80 --frame-duration 40 --pause-duration 2000 --power 4 --max-size 800 --loop 0 --quality 90
```

## License

This project is open-source and available under the [MIT License](LICENSE).

