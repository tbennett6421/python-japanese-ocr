# Japanese OCR in Python

## Dependencies

- Python 3
- Scipy
- OpenCV >= 4
- Tesseract (see below)

### Tesseract

- Install `tesseract` 4.0
- Download `jpn_vert.traineddata` [here](https://github.com/tesseract-ocr/tessdata/blob/master/jpn_vert.traineddata)
- Copy `jpn_vert.traineddata` in `/usr/share/tessdata`
- Check with `tesseract --list-langs` that `jpn_vert` correctly appears

### Ubuntu / Mint

```sh
sudo apt-get install -y tesseract-ocr tesseract-ocr-jpn-vert
python3 -m venv env
source env/bin/activate
# Upgrade pip per opencv-python FAQ
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## How to use

```py
./main.py examples/sample_page.jpg
```

Followed by:

```py
./main.py examples/sample_page.jpg --ocr
```

