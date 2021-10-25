# gif

gitfiti noun : Carefully crafted graffiti in a github commit history calendar.

An example of gitfiti in the wild:
alt text

gitfiti.py is a tool I wrote to decorate your github account's commit history calendar by (blatantly) abusing git's ability to accept commits in the past.

How? gitfiti.py generates a bash script: gitfiti.sh that makes commits with the GIT_AUTHOR_DATE and GIT_COMMITTER_DATE environment variables set for each targeted pixel.

Since this is likely to clobber repo's history, I highly recommend that you create a new github repo when using gitfiti. Also, the generated bash script assumes you are using public-key authentication with git.

Pixel Art:
alt text
Included "art" from left to right: kitty, oneup, oneup2, hackerschool, octocat, octocat2

Usage:
Create a new github repo to store your handiwork.
Run gitfiti.py and follow the prompts for username, art selection, offset, and repo name.
Run the generated gitfiti.sh from your home directory (or any non-git tracked dir) and watch it go to work.
Wait... Seriously, you'll probably need to wait a day or two for the gitfiti to show in your commit graph.
User Templates
The file format for personal templates is the following:

Each template starts off with a ":" and then a name (eg. ":foo")
Each line after that is part of a json-recognizable array.
The array contain values 0-4, 0 being blank and 4 being dark green.
To add multiple templates, just add another name tag as described in 1.
For example:

:center-blank
[[1,1,1,1,1,1,1],
[1,1,1,1,1,1,1],
[1,1,1,1,1,1,1],
[1,1,1,0,1,1,1],
[1,1,1,1,1,1,1],
[1,1,1,1,1,1,1],
[1,1,1,1,1,1,1]]
This would output a 7 x 7 light green square with a single blank center square.

Once you have a file with templates, enter its name when prompted and the templates will be added to the list of options.

Removal:
Fortunately if you regret your gitfiti in the morning, removing it is fairly easy: delete the repo you created for your gitfiti (and wait).

License:
gitfiti is released under The MIT license (MIT)

Todo:
Remove 'requests' dependency thanks empathetic-alligator
Web interface See several web-based things below
Load "art" from a file thanks empathetic-alligator
Load commit content from a file
Text/alphabet option
...
Profit?
Notable derivatives or mentions:
Pikesley's Pokrovsky, which offers Github History Vandalism as a Service!
github-board commits gitfiti from easy templates
ghdecoy fills the contribution graph with random data (sneaky!)
Gitfiti Painter visual drawing tool for artists to easily create templates
git-draw a Chrome extension which will allow you to freely draw on your commit map(!)
github-jack a pure bash version with space invaders and shining creepypasta
Seen something else? Submit a pull request or open an issue!
