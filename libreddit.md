version: "3"
services:
#--------------------------------------------------------------------------------------------#
#                                  Libreddit                                                 #
#--------------------------------------------------------------------------------------------#
  libreddit:
    container_name: libreddit
    image: spikecodes/libreddit:arm
    restart: unless-stopped
    ports:
      - '8005:8080'
    environment:
      - LIBREDDIT_DEFAULT_SHOW_NSFW=on      # Turn on 18+ content
      - LIBREDDIT_DEFAULT_USE_HLS=on        # HLS Video
      - LIBREDDIT_DEFAULT_THEME=black       # Theme
      - LIBREDDIT_DEFAULT_AUTOPLAY_VIDEOS=off # No autoplay
      - LIBREDDIT_DEFAULT_THEME=gold        # Gold
      - LIBREDDIT_DEFAULT_FRONT_PAGE=all    # r/all
