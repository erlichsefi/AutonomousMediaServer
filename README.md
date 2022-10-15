This is a new version of the autonumos stream dockers.

Trassmission Docker for downloading torrents:
    - with additional script that unzip session packs.
      script: resources/scripts/unzip.sh
      setting: resources/trassmission/torrent_config/settings.json:script-torrent-done-filename
      
        "script-torrent-done-enabled": true,
        "script-torrent-done-filename": "scripts/unzip.sh",
       

Jacket Docker that track torrent sources:
  - hebits
  - torrentleech
  - add more ...

  ** please make sure your config torrent trackers and not other kinds.


Sonarr Docker that manage TV shows:
1. Read http://trakt.tv/ for new TV shows to be tracked. # configure from the UI
2. Track episodes for each series (new eposide and already aired)
3. Fetch Torrent from Jacket. # configure from the UI
4. Sent to Transmission. # configure from the UI
5. Watch Transmission download folder and mange '${VIDEO_PATH}/tv' folder. # configure from the UI


Ranarr Docker that manage movies:
1. Read http://trakt.tv/ for new movies to be tracked.  # configure from the UI
2. Fetch Torrent from Jacket. # configure from the UI
4. Sent to Transmission. # configure from the UI
5. Watch Transmission download folder and mangew '${VIDEO_PATH}/movies' folder. # configure from the UI

Flex docker that manage a media server and track watch:
Track to following folders.
 - ${VIDEO_PATH}/movies
 - ${VIDEO_PATH}/tv



Bottom line,
I'm adding Movies/Tv shows to trakt.tv list, 24 hours later i can watch them in my android Flex client, every new episode that air is download automatically. 