# Wikidata bot to add MBIDs

## Installation

This needs both `psycopg2` and
[pywikipediabot](https://www.mediawiki.org/wiki/PWB) (core repository).

The former can be installed with

> pip install -r requirements.txt

the latter with

> git clone --recursive https://gerrit.wikimedia.org/r/pywikibot/core.git pywikipediabot
>
> cd pywikipediabot
>
> python2 setup.py install

Copy `bot/settings.py.dist` to `bot/settings.py` and edit the connection string
which is documented
[here](http://www.postgresql.org/docs/current/static/libpq-connect.html#LIBPQ-CONNSTRING).

If you want the bot to automatically edit URLs to redirect pages in Wikipedia to
their target pages, do

> git submodule init
>
> git submodule update

and set the `mb_user` and `mb_password` values in `bot/settings.py` to your bots
login data in MusicBrainz.

Please make sure that your bot does not violate the
[Code of Conduct](https://musicbrainz.org/doc/Code_of_Conduct/Bots) for bots in MusicBrainz
