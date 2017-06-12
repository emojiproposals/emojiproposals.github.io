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

Install some stuff needed by `nokogiri`, because I've found that it will never install otherwise.

```bash
sudo apt-get install libxslt-dev libxml2-dev
```

Then install all the gems (and also make `nokogiri` use the libs we just installed):

```bash
NOKOGIRI_USE_SYSTEM_LIBRARIES=1 bundle install
```
