```yml
version: "3"
services:
#--------------------------------------------------------------------------------------------#
#                                  Libreddit                                                 #
#--------------------------------------------------------------------------------------------#
  libreddit:
    container_name: libreddit
    # libreddit:armv7 and libreddit:latest (Amd64) also available.
    image: spikecodes/libreddit:arm
    restart: unless-stopped
    ports:
      - '7010:8080'
    environment:
      - LIBREDDIT_DEFAULT_SHOW_NSFW=on      # Turn on 18+ content
      - LIBREDDIT_DEFAULT_USE_HLS=on        # HLS Video
      - LIBREDDIT_DEFAULT_THEME=black       # Theme
      - LIBREDDIT_DEFAULT_AUTOPLAY_VIDEOS=off # No autoplay
      - LIBREDDIT_DEFAULT_THEME=gold        # Gold
      - LIBREDDIT_DEFAULT_FRONT_PAGE=all    # r/all
```
