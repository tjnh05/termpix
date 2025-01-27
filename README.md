# termpix

Draw images in an ANSI terminal! Requires that your terminal can show ANSI colours, and uses a font that can show the 'bottom half block' character (▄).

Usage:
```text
python3.9 termpix.py <filename|url> [--true-color|--true-colour]  [--output output.txt] \
          [--width <width>] [--height <height>]
```
filename or url can be any `image` file readable by the python 'PIL' library or can be any `video` file readable by `imageio`. It also supports HEIC format, if `pyheif` and `libffi libheif` are installed. If you type camera as the filename, you can view your webcam video.

It will fill as much of the terminal as possible, while keeping the aspect ratio of the input image. Use --width or --height to override this.

Try this command:
```bash
python3.9 termpix.py \
  https://img.blogs.es/anexom/wp-content/uploads/2020/10/mario-destacada_E.jpg \
  --true-color
```
And you will see:

[![asciicast](https://asciinema.org/a/cEW7FK66bmr0wsmRNcMpocx1D.svg)](https://asciinema.org/a/cEW7FK66bmr0wsmRNcMpocx1D)

This library is also extended to play video in terminal (with audio), you can try the
```text
python3.9 termpix.py <mp4_filename>
```

[![asciicast](https://asciinema.org/a/yuogBz7sZaSwLmRBN4BGcTv6v.svg)](https://asciinema.org/a/yuogBz7sZaSwLmRBN4BGcTv6v)

This project is much inspired by the following repository:
- https://github.com/hopey-dishwasher/termpix

# Installation
for ubuntu, perform commands below to install software packages at first:
```bash
sudo apt-get install -y portaudio19-dev ffmpeg
```
then install python packages (recommend to install them in your own virtual environment, python3.x):
```bash
pip3 install -r requirements.txt
```

# License
Apache 2.0 license
