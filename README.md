What is this?
I made an ebuild for Maya 2012 for Gentoo, it’s quite ugly but it seems to work for me. Please tell me if you got problems. Please fork me to fix stuff. You still need to run the graphical installer to make stuff work, I’m not sure about what happens there yet… The ebuild will tell you the details after the install…

How to add it to my system?
Merge layman (with git enabled ofc), edit the file: /etc/layman/layman.cfg

And add https://github.com/tux1989/maya2018/raw/master/overlay.xml to the overlays: part.

So it looks like this…

overlays  : http://www.gentoo.org/proj/en/overlays/repositories.xml
  https://github.com/tux1989/maya2018/raw/master/overlay.xml
And then just…

# layman -L
# layman -a maya
And make sure to have this at the end of your /etc/make.conf:

# source /var/lib/layman/make.conf
Or if you just need to use it quick, do it this way:

# layman -f -a maya -o https://raw.github.com/tux1989/maya2018/master/overlay.xml# maya2018
