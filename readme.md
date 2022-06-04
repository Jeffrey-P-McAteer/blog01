
# Blog02

Another attempt to run a wysiwyg software that spits out a static blog.

# Setup

1. Install python
    - `yay -S python`
2. Install Lektor
    - `python -m pip install --user Lektor`
3. Create a new blog in the folder `./mysite`
    - `python -m lektor --project ./mysite quickstart`
4. Run the wysiwyg editor
    - `python -m lektor --project ./mysite server`
    - Open `http://127.0.0.1:5000` in a browser to make blog edits
5. Once you like it, build it. `./mysite/mysite_www/` will hold the static contents
    - `python -m lektor --project ./mysite build --output-path ./mysite_www`

6. For advanced changes like modifying the pages in the bar shown at the top, see the `./mysite/templates/` directory.
   This will require some .html knowledge, but once you have templates you like it's easy to use them from the wysiwyg editor
   by editing the article, opening "System Fields", and typing in the template file name under "Template". Most pages default to using `page.html`.
    - This is also how you'd do things like set a page-wide background image or apply a page-wide css style.


