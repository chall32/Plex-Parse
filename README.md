Plex-Parse
==========

## Plex Library to comma separated variables (.csv) file 
Chris Hall & John Stallan 2010-2014 - [chall32.blogspot.com]

### What is Plex?
[Plex] is a media player system and software suite consisting of a player applications and an associated media server that organises personal media stored on local devices

### What does Plex-Parse do?
Plex-Parse converts a saved copy of your Plex Media Server library section xml into a .csv file.  This .csv can then be opened and manipulated using any spreadsheet application (for example Microsoft Excel, Libre Office Calc etc) 

### Why?
Sometimes it is easier, to browse and manipulate your plex library section when it is in spreadsheet format 

###Pre-Requisites
1.  Powershell - you need to be running Windows 7 or newer to use this program. I recommend running Plex-Parse.ps1 in [PowerShell ISE]
2.  A Plex Media Server!

### How to Use
1.  Open http://(your plex media server):32400/library/sections/
2.  Find the location id of the library location that you are interested in exporting.  For example:

``` 
<Directory allowSync="0" art="/:/resources/movie-fanart.jpg" filters="1" refreshing="0" 
thumb="/:/resources/movie.png" key="2" type="movie" title="Family Movies" 
agent="com.plexapp.agents.themoviedb" scanner="Plex Movie Scanner" language="en" 
uuid="XXYYZZ" updatedAt="1234567890" createdAt="1234567890"> 
<Location id="2" path="D:\Movies"/> </Directory>
```

In this case my location id is 2

3.  Open http://(plex server):32400/library/sections/(section id)/all/ 
        (eg http://127.0.0.1:32400/library/sections/2/all/ )
4.  Save this as **Library.xml** into the same directory as your downloaded copy of Plex-Parse.ps1
5.  Open Plex-Parse.ps1 with Powershell ISE and hit F5 or the green play button.
6.  Your csv output file will be saved as **Library.csv**  in the same directory as your downloaded copy of Plex-Parse.ps1
7.  Repeat steps 1 to 6 for any other Plex library sections you are interested in exporting to csv

### What's New?
***See the [changelog] for what's new in the most recent release.***


### [Click here to download latest version](https://github.com/chall32/plex-parse/blob/master/Plex-Parse.ps1?raw=true)

If Plex-Parse helped you, how about buying us a beer? Use the donate button below. THANK YOU!

[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=KT462HRW7XQ3J)

[PowerShell ISE]:http://blogs.technet.com/b/heyscriptingguy/archive/2012/02/07/learn-how-to-use-the-free-powershell-ise-to-edit-scripts.aspx
[changelog]: https://github.com/chall32/plex-parse/blob/master/ChangeLog.txt
[chall32.blogspot.com]: http://chall32.blogspot.com
[Plex]:https://plex.tv/
