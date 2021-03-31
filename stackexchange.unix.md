To list the available formats type:

    youtube-dl -F url

Then you can choose to download a certain format-type by entering the number for the format code (in the sample below `11`): 

    youtube-dl -f 11 url 

Example from [webupd8][1]

    youtube-dl -F http://www.youtube.com/watch?v=3JZ_D3ELwOQ
sample output:

    [youtube] Setting language
    [youtube] 3JZ_D3ELwOQ: Downloading webpage
    [youtube] 3JZ_D3ELwOQ: Downloading video info webpage
    [youtube] 3JZ_D3ELwOQ: Extracting video information
    [info] Available formats for 3JZ_D3ELwOQ:
    format code extension resolution  note 
    171         webm      audio only  DASH webm audio , audio@ 48k (worst)
    140         m4a       audio only  DASH audio , audio@128k
    160         mp4       192p        DASH video 
    133         mp4       240p        DASH video 
    134         mp4       360p        DASH video 
    135         mp4       480p        DASH video 
    136         mp4       720p        DASH video 
    137         mp4       1080p       DASH video 
    17          3gp       176x144     
    36          3gp       320x240     
    5           flv       400x240     
    43          webm      640x360     
    18          mp4       640x360     
    22          mp4       1280x720    (best)

You can choose `best` and type

    youtube-dl -f 22 http://www.youtube.com/watch?v=3JZ_D3ELwOQ

> To get the best video quality (1080p DASH - format "137") and best audio quality (DASH audio - format "140"), you must use the following command:

    youtube-dl -f 137+140 http://www.youtube.com/watch?v=3JZ_D3ELwOQ

**EDIT**

You can get more options [here][2]

Video Selection:

    --playlist-start NUMBER          Playlist video to start at (default is 1)
    --playlist-end NUMBER            Playlist video to end at (default is last)
    --playlist-items ITEM_SPEC       Playlist video items to download. Specify
                                 indices of the videos in the playlist
                                 separated by commas like: "--playlist-items
                                 1,2,5,8" if you want to download videos
                                 indexed 1, 2, 5, 8 in the playlist. You can
                                 specify range: "--playlist-items
                                 1-3,7,10-13", it will download the videos
                                 at index 1, 2, 3, 7, 10, 11, 12 and 13.
    --match-title REGEX              Download only matching titles (regex or
                                 caseless sub-string)
    --reject-title REGEX             Skip download for matching titles (regex or
                                 caseless sub-string)
    --max-downloads NUMBER           Abort after downloading NUMBER files
    --min-filesize SIZE              Do not download any videos smaller than
                                 SIZE (e.g. 50k or 44.6m)
    --max-filesize SIZE              Do not download any videos larger than SIZE
                                 (e.g. 50k or 44.6m)
    --date DATE                      Download only videos uploaded in this date
    --datebefore DATE                Download only videos uploaded on or before
                                 this date (i.e. inclusive)
    --dateafter DATE                 Download only videos uploaded on or after
                                 this date (i.e. inclusive)
    --min-views COUNT                Do not download any videos with less than
                                 COUNT views
    --max-views COUNT                Do not download any videos with more than
                                 COUNT views
    --match-filter FILTER            Generic video filter (experimental).
                                 Specify any key (see help for -o for a list
                                 of available keys) to match if the key is
                                 present, !key to check if the key is not
                                 present,key > NUMBER (like "comment_count >
                                 12", also works with >=, <, <=, !=, =) to
                                 compare against a number, and & to require
                                 multiple matches. Values which are not
                                 known are excluded unless you put a
                                 question mark (?) after the operator.For
                                 example, to only match videos that have
                                 been liked more than 100 times and disliked
                                 less than 50 times (or the dislike
                                 functionality is not available at the given
                                 service), but who also have a description,
                                 use --match-filter "like_count > 100 &
                                 dislike_count <? 50 & description" .
    --no-playlist                    Download only the video, if the URL refers
                                 to a video and a playlist.
    --yes-playlist                   Download the playlist, if the URL refers to
                                 a video and a playlist.
    --age-limit YEARS                Download only videos suitable for the given
                                 age
    --download-archive FILE          Download only videos not listed in the
                                 archive file. Record the IDs of all
                                 downloaded videos in it.
    --include-ads                    Download advertisements as well
                                 (experimental)


  [1]: http://www.webupd8.org/2014/02/video-downloader-youtube-dl-gets.html
  [2]: https://github.com/ytdl-org/youtube-dl#video-selection
