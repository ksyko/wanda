# wanda
Script to set wallpaper using keyword or randomly

![Codacy branch grade](https://img.shields.io/codacy/grade/e5aacd529ce04f3fb8c0f9ce6a3bdd9e/main)
![PyPI](https://img.shields.io/pypi/v/wanda)
![PyPI - Downloads](https://img.shields.io/pypi/dw/wanda)
![PyPI - License](https://img.shields.io/pypi/l/wanda)
![Gitlab code coverage](https://img.shields.io/gitlab/coverage/kshib/wanda/main)
![Gitlab pipeline](https://img.shields.io/gitlab/pipeline-status/kshib/wanda?branch=main)

## Installation / Update
```
pip install wanda -U
```

For termux, you will need the following packages:
```
pip install --upgrade pip
pkg in libxml2 libxslt libjpeg-turbo
```

For issues installing pillow refer this [document](https://pillow.readthedocs.io/en/stable/installation.html)


## Usage
```
wanda
wanda -t mountain
wanda -s earthview
wanda -s wallhaven -t japan
```
`wanda -h` for more details

## Notes
- By default, the source is [unsplash](https://unsplash.com).
- Some sources may have inapt images. Use them at your own risk.

## Supported sources

- [4chan](https://boards.4chan.org) via [Rozen Arcana](https://archive.alice.al)
- [500px](https://500px.com)
- [artstation](https://artstation.com)
- [imgur](https://imgur.com) via [rimgo](https://rimgo.pussthecat.org)
- [earthview](https://earthview.withgoogle.com)
- local
- [picsum](https://picsum.photos)
- [reddit](https://reddit.com)
- [unsplash](https://unsplash.com)
- [wallhaven](https://wallhaven.cc)

## Automate (For linux)
* To set wallpaper at regular intervals automatically:

0. (For termux) Install:
```
termux-wake-lock
pkg in cronie termux-services nano
sv-enable crond
```
1. Edit crontab
```
crontab -e
```
2. Set your desired interval. For hourly:
```
@hourly wanda -t mountains
```
[(more examples)](https://crontab.guru/examples.html)

4. ctrl+o to save, ctrl+x to exit the editor

## Build
[python](https://www.python.org/downloads/) and [poetry](https://python-poetry.org/) are needed
```
git clone https://gitlab.com/kshib/wanda.git && cd wanda
poetry install
poetry build
```

## Uninstall
```
pip uninstall wanda
```

## Shell
Older versions can be found [here (android)](https://gitlab.com/kshib/wanda/-/tree/sh-android) and [here (desktop)](https://gitlab.com/kshib/wanda/-/tree/sh-desktop)

## Issues
The script is tested on Manjaro+KDE and Android+Termux and Windows 11.

On Windows, you might need to set wallpaper mode to slideshow with folder as `C:\Users\%username%\wanda`

## License
MIT
