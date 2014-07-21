This is a Python 2.x WSGI version of https://github.com/fehmicansaglam/progressed.io, so all credit
for the idea and original implementation is due to Fehmi Can Sağlam.

I wrote it as a little snack of sorts, but it may be useful for understanding how to write very simple
raw WSGI apps in Python. :)

Unlike the original, the application itself will not bother with compressing the result, expecting
it to be the duty of the the frontend HTTP server.

The source code fully conforms to PEP 8, aside from the SVG literal having an over-long line. :) 

Usage:

* You may run `progressed.py` directly via Python, in which case it will bind the default Python
  `wsgiref.simple_server` server to 0.0.0.0:8080 and serve progress bars at `/bar/<progress>`.
* If you use uWSGI, `uwsgi --wsgi progressed --http 0.0.0.0:8080` should get you running.
