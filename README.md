## Blink

Blink is a simple single or bulk webpage screenshotting tool, often used for reconnaissance/archival (OSINT) purposes.

### Requirements

`pipenv install`

If you do not have `pipenv` installed, first install it with `pip3 install pipenv`.

### Usage

```console
Usage: blink.py [OPTIONS]

Options:
  -it, --input_type TEXT  type of the input (can be single/bulk followed by the url/textFile).  [required]
  -o, --output TEXT       name of the folder to save the screenshots to.
                          [default: screenshots]
  -ws, --windowsize TEXT  window size of the screenshot.  [default: 1200x600]
  -to, --timeout INTEGER  webpage request timeout in seconds.  [default: 10]
  -h, --help              Show this message and exit.
```

### Example

```console
python3 blink.py -it single acme.com -o example -ws 1920x1080 -to 5

[:] Creating example folder...
[:] Processing 1 URL(s)
[1/1] Opening acme.com
[:] Done processing example.txt

python3 blink.py -it bulk example.txt -o example -ws 1920x1080 -to 5

[:] Creating example folder...
[:] Processing 1 URL(s)
[1/1] Opening acme.com
[:] Done processing example.txt
```



### Format

Text file format:

```txt
acme.com
google.com
yahoo.com
```

---

&copy; 2018 Leonid Hartmann
