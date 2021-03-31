#### Wallpaper auto change

https://unix.stackexchange.com/questions/397169/

FEH

https://packages.debian.org/stretch/feh


------------------------------------------------------------------------------------------



`echo` could be replaced w/ `<<<` too, but then quotation marks are needed und the simplicity of termbin isn't obvious any more.
At first glance I did't recognize whether it's the number '1' or the letter 'l' in 'l.termbin.com' and 




------------------------------------------------------------------------------------------


#### termbin.com

## Easy way to paste command line output to paste bin services?

https://unix.stackexchange.com/questions/108493/easy-way-to-paste-command-line-output-to-paste-bin-services
https://unix.stackexchange.com/posts/154930/edit

```
I needed something to share terminal output even when X server wasn't loaded so I created this service: [termbin.com][1]. The only thing you need is netcat, then you can easily share with anyone anything that can be shown in terminal, there's example:

    nc termbin.com 9999 < /etc/fstab
    nc termbin.com 9999 

After running this command you'll get in response url address with text file.

To make your life easier you can add such alias to your .bashrc file:

    echo 'alias tb="nc termbin.com 9999"' >> .bashrc

Now sharing will be much simplier:

    uname -a | tb

You can get saved ones for example by using curl. You'll find more examples on [termbin.com][1].

You can host your own server as well, there is github repository: [https://github.com/solusipse/fiche][2]. If you want to make it private, don't forget to set whitelist parameter.


  [1]: http://termbin.com
  [2]: https://github.com/solusipse/fiche
  ```

------------------------------------------------------------------------------------------


#### SENT
#### youtube-dl

## Download only format mp4 on youtube-dl
https://unix.stackexchange.com/questions/272868/download-only-format-mp4-on-youtube-dl
https://unix.stackexchange.com/posts/272934/edit


  [2]: https://github.com/ytdl-org/youtube-dl#video-selection

Fix youtube-dl URL; point link fragment to 'Video Selection'.
