# mimecdn
Client-side tool for showing HTML files on GitHub

## How to use

Visit `https://embeddedt.github.io/mimecdn/index.html?rawurl=<your raw GitHub URL>`.

Example: https://embeddedt.github.io/mimecdn/index.html?rawurl=https://raw.githubusercontent.com/littlevgl/lv_micropython/dev-6.0/ports/javascript/lvgl_editor.html

## How does it work?

Normally, when accessing raw HTML files on GitHub, they are served with a MIME type of `text/plain`. This tells the browser not to actually treat the file as HTML, but rather as a plaintext file (`.txt`).

MimeCDN gets around this issue by ignoring the MIME type, and manually reading the file. (This is where the name "MimeCDN" came from.) The contents of the MimeCDN document are then replaced by the contents of your URL. The code's pretty simple and self-explanatory; you can read that for more information.

One cool thing about MimeCDN is that there is no server-side logic happening. All of this is handled directly within your browser. No extensions or anything special is required. Just fill in the `rawurl` query parameter with your URL, and everything is handled automagically.

## Limitations

Currently, this only works with plain HTML. CSS might work but could have issues. JavaScript won't work properly in most (all?) cases.
