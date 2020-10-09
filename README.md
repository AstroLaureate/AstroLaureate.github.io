# AstroLaureate

### Installing everything you need for the website to build locally:

1. Make sure you have ruby installed. If you can `ruby -v` in cmd/terminal, you're good. Otherwise, head [to here](https://www.ruby-lang.org/en/documentation/installation/). Make your life easy and install the toolchain (ruby-dev) as well.
2. Check out the repo
3. Go to the repo and open cmd/terminal, and run:
4. `gem install bundler`
5. Then run `bundle install`

### Starting the server locally

Run either `runLocal.bat` or `runLocal.sh` depending on your OS. It should auto update, so if you make
changes to a post, if you wait a second or two and refresh the website it should have updated.

### Adding or editing a new person

1. Make a new markdown file under the relevant folder (`_people` for a new person, or look under `_posts` for news or projects)
2. Fill out the info at the top however you want
3. The `loc` property tells the site where to look for media like images, so under `static/img/<loc>`, you can put your images, videos, etc
4. For people, "rank" determines sorting order. 50 for Tam, 40 for postdocs, 30 for PhD Candidates, 20 for Honours, and we can fine tune.
5. Commit and push. Make sure your images are added to git. Everything on master will appear on the primary website within a few minutes.

Notes: main.jpg images are 700x700 pixels, and thumb_cards are 600x400 pixels. 

### Things you can do in a post

1. Markdown. All your normal markdown syntax works.
2. Include images, via the `{% include image.html ... %}` syntax
3. Include videos, via the `{% include video.html ... %}` syntax
4. Include Youtube videos, via the `{% include youtube.html ... %}` syntax
5. Include presentations (like Google slides), via the `{% include presentation.html ... %}` syntax
6. Include PDF documents, via the  `{% include pdf.html ... %}` syntax
6. Include a carousel of images, via the  `{% include carousel.html ... %}` syntax
7. Include your own custom HTML to do whatever you want

All of the includes you can see in the `_includes` directory. If you want more, just write up a
new html file in the `_includes` directory (or send a message to Sam who can help out with that)

### I want to change how things look

Welcome to CSS. `style.css` is where its at. The site has an old Bootstrap 3 css framework, so you can
use any of those helper classes when customising. For an example, notice in each persons profile 
I added a div to center some of the text at the top.

### I want to add a new paper

Open up the `_data/papers.yml` file and add a new entry.