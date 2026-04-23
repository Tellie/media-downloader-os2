===================================================================================================
**** If you like the programs i'm porting and you want to donate to me, see the following URL: ****
**** http://www.bitwiseworks.com/shop/index.php?id_product=38&controller=product& id_lang=1    ****
****             Or send directly to me using PayPal: tellie@elbertpol.nl                      ****
****                All the money you send will go to the QT5 project                          ****
===================================================================================================

Media-downloader v5.5.2   

 CONTENTS OF THIS FILE
 =====================

1. INTRODUCTION

2. REQUIREMENTS

3. INSTALLATION

4. LICENSE, COPYRIGHT, DISCLAIMER

5. CONTACT

6. CREDITS

7. SUPPORT AND DONATIONS

8. HISTORY

9. RESTRICTIONS


1. INTRODUCTION
===============

Welcome to media-downloader v5.5.2 port for OS/2 and Arcanoae.

This project is a Qt/C++ based GUI frontend to CLI multiple CLI-based tools that deal with downloading online media.11

[yt-dlp](https://github.com/yt-dlp/yt-dlp) CLI tool is the default supported tool and other tools can be added by
downloading their extension and a list of supported extensions is managed
[here](https://github.com/mhogomchungu/media-downloader/wiki/Extensions).

2. REQUIREMENTS
===============
  The following requirements can be installed either by rpm or by zip files  

  RPM Installation (preferred):
  ============================
  klibc
  -----
   1. yum install libc
  
  
  --------
   1. yum install libgcc1
   2. yum install libssp
   3. yum install libstdc++6 libstdc++
   4. yum install libsupc++6 libsupc++
   5. yum install libgcc-fwd

  Qt5 dll
  -------
   1. yum install Qt5Core Qt5Gui Qt5Wdgt Qt5Net

    
  Zlib  
  ----
   1. yum install zlib

3. INSTALLATION
===============

  Media-downloader
  ---
  1. It's create a directory for Media-downloader.
  2. It's create a WPS object for Media-downloader.exe.
  3. It's create a map for Media-downloader

4. LICENSE, COPYRIGHT, DISCLAIMER
=================================

(C) 2007-2024 mhogomchungu@gmail.com https://github.com/mhogomchungu/media-downloader

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.


5. CONTACT
==========

if you find a bug, then add a ticket to the trac at http://svn.netlabs.org/qtapps

Only bug reports with a reproducable bug are accepted. :-)



6. CREDITS
==========

The port was done by: Elbert Pol aka TeLLie

Thanks go to:

  * Francis Banyikwa
  * Dmitry A. Kuminov
  * Silvan Scherrer

They either helped me when I had some nasty questions or did some testing for me.


7. SUPPORT AND DONATIONS
========================

Tea is based on volunteer work. If you would like to support further
development, you can do so in one of the following ways:


  * Donate to the Qt5 project

  * While working on Qt 5 for OS/2, we are glad to know that our work is being partly sponsored by the grateful OS/2 community.
    Given the scale of this project and all other OS/2 projects that we work on, and also the fact that the OS/2 world has limited financial resources nowadays, every penny counts.
    We need to pay our full-time and part-time developers for their hard work. So any contribution is highly appreciated!
    To do so, please visit our online shop where you can buy development units of a preferred value.
    https://www.bitwiseworks.com/shop/index.php

  * Contribute to the project: Besides actual development, this also includes maintaining the documentation and the project web site as well as help for users.

8. HISTORY
==========
Compiled now with Qt v5.15.2

Changelog:
     Version 5.5.0(March 14th, 2026)
     [FLATPAK]
      - Bundle svtplay-dl because its dependencies are now bundled too.
     [ALL]
      - Show more info in batch downloader when using svtplay-dl.

     Version 5.5.1(April 14th, 2026)
     [FLATPAK]
      - Continue to bundle svtplay-dl dependencies but unbundle svtplay-dl executable.
     [ALL]
      - Add GUI options to tell MD to use system binaries or to download its own binaries.

     Version 5.5.2(April 23rd, 2026)
     [ALL]
      - Fix a bug that made it impossible to update Deno from within the application.
      - When showing a list of available media, show audio language below format code if it is available.

How to install:

If you get error that it cannot download yt-dlp then you have to set in ?:\Home\.local\share\media-downloader\settings\settings.ini to NetworkTimeOutInSeconds=300
REQUIREMENTS

PYTHON3
You need python 3 to run this software, you can get it from the netlabs rpm, but sometimes there are a conflict issue to install this software.
The issue was listed here: https://mantis.arcanoae.com/view.php?id=3523

The trick to install python 3 is:
- In ANPM (Arca Noae Package Manager) go to "Available - RPM"
- Select "python2.7", "python3", "python-unversioned-command" and run "Install".
It will take some time while it obsolete some packaged and get the new ones.
After that you will be able to run Media-Downloader and will automatically download "yt-dlp runtime" that is required.

CONFIGURATION CHANGES
'By default, youtube-dl and its forks create files that are in title-id.extension format and what you seem
to not want is the id part and you can remove it by doing the following:-

On OS2 we cant have utf8 filenames, and we need to stick with ascii, that's why we need to
add --restrict-filenames 

- Go to Configure tab.
- Go to Engines's Default Options tab.
- At the Engine's Name drop down list, select an engine you want to change its option.
- At the "Options To Add" text field, add  --newline --ignore-config --no-playlist --restrict-filenames -o %(title).200s-%(id)s.%(ext)s
- Click Add.
- Right click the newly added entry and then select Set As Default.
Now you won't get an error while trying to download the file. 

