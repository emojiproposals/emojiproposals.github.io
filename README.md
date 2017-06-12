# Emoji Proposals (an art blog)

## Installing the stuff

Install `ruby`. I recomment using [`rvm`](https://rvm.io/). (Also, I've only done this on Linux... so deal with it.)

Install `bundler`:

```bash
gem install bundler
```

Createa a gemset (whatever that is):

```bash
rvm gemset create emojiproposals
rvm gemset use emojiproposals
```

Install some stuff needed by `nokogiri`, because I've found that it will never install otherwise:

```bash
sudo apt-get install libxslt-dev libxml2-dev
```

Then install all the gems (and also make `nokogiri` use the libs we just installed):

```bash
NOKOGIRI_USE_SYSTEM_LIBRARIES=1 bundle install
```

## Running the site locally

Did you finally manage to install everything? Yeah, I know, it was hard. It's okay though, because you are now ready to write about art. Just one more quick step:

```bash
jekyll serve
```

Now, you can browse to the URL that the command prints out -- usually [`http://127.0.0.1:4000/`](http://127.0.0.1:4000/) (I even made that a link, just for you).

## Writing stuff

Apparently, whatever `jekyll` uses for markdown has comments... like this:

```
{% comment %}
This is a comment
{% endcomment %}
```

Probably not a good idea to use this though...
