This is a new version of the autonumos stream dockers.

Trassmission Docker for downloading torrents
    - with additional script that unzip session packs.
      script: resources/scripts/unzip.sh
      setting: resources/trassmission/torrent_config/settings.json:script-torrent-done-filename
      
        "script-torrent-done-enabled": true,
        "script-torrent-done-filename": "scripts/unzip.sh",
       


Jacket Docker that track two sources:
  - hebits
  - torrentleech

  ** please notice to config torrent trackers and not other kinds.

Sonarr Docker that manage TV shows:
1. Read http://trakt.tv/ for new TV shows to be tracked.
2. Track episodes for each series (new eposide and already aired)
3. Fetch Torrent from Jacket.
4. Download and manage TV show folder

Ranarr Docker that manage movies:
1. Read http://trakt.tv/ for new movies to be tracked.
2. Fetch Torrent from Jacket.
3. Download and manage Movie folder

Flex docker that manage a media server and track watch.


Bottom line,
I'm adding Movies/Tv shows to trakt.tv list, 24 hours later i can watch them in my android Flex client, every new episode that air is download automatically. 