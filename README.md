This is a new version of the autonumos stream dockers.

Service #1: Trassmission Docker for downloading torrents:
    
    your job: 
    with additional script that unzip session packs.
      script-path= resources/scripts/unzip.sh
      In setting (resources/trassmission/torrent_config/settings.json:script-torrent-done-filename) add the script script-path
      
        "script-torrent-done-enabled": true,
        "script-torrent-done-filename": "scripts/unzip.sh",
       

Service #2: Jacket Docker that track torrent sources:
  - hebits
  - torrentleech
  - add more ...

  your job: 
  please make sure you configure torrent trackers in Jacket, whatever you want.


Service #3: Sonarr Docker that manage TV shows:
1. Read http://trakt.tv/ for new TV shows to be tracked. # your job: configure sonarr to read trakt
2. Track episodes for each series (new eposide and already aired)
3. Fetch Torrent from Jacket. # your job: configure sonarr to query jacket
4. Sent to Transmission.  # your job: configure in sonarr download client as transmission
5. Watch Transmission download folder and mange '${VIDEO_PATH}/tv' folder. # your job: add path to plex


Service #4: Ranarr Docker that manage movies:
1. Read http://trakt.tv/ for new movies to be tracked.  # your job: configure radarr to read trakt
2. Fetch Torrent from Jacket. # your job: configure radarr to query jacket
4. Sent to Transmission. # your job: configure in radarr download client as transmission
5. Watch Transmission download folder and mange '${VIDEO_PATH}/movies' folder.  # your job: add path to plex

Service #5: Flex docker that manage a media server and track watch:
Track to following folders.
 - ${VIDEO_PATH}/movies
 - ${VIDEO_PATH}/tv



Bottom line,
I'm adding Movies/Tv shows to trakt.tv list, 24 hours later i can watch them in my android Flex client, every new episode that air is download automatically. 