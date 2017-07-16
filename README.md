# FreeBSD-Mod-makefiles
My own adjustments to Makefiles for FreeBSD ports, to remove dependencies or for other improvements.

Due to my own frustration that some ports include gratuitous dependencies, I began creating a revised Makefile for each which successfully removed them.  As an example, I do not use KDE as my desktop environment but utilities (Kate is one) built to run under KDE assume certain daemons or other functions (kactivities) that will not exist on my system and are otherwise entirely unneeded.  

The Makefiles are named for their port-origin and rather than using a diff system, they simply replace the former Makefile.  A script to automate this replacement process will eventually be crafted and included, a diff method may be developed at a later date.  This script might also eventually take advantage of the FreeBSD Makefile system so that I could offer an options config checkbox list with descriptions for each as needed, in which case this whole thing could operate like a normal port, even if it is not positioned into the ports tree officially.

Of course I could spend time chatting with port maintainers or pick up the maintainership of any port, but since I tend to be a solitary operator wishing my own odd variation on my box which could break many things.. well, for the moment at least this is my personal solution to my frustration and a guaranteed fix that I do not need to wait to be approved or applied to any port.

## Future concept
A universal configuration makefile options config. Here you would choose what sound system to use, which browser, yadda yadda, and all conflicts and redundancies would be handled.  Yes, it is possible via /etc/make.conf to set or unset various options but without having exhaustively researched each and every possible interdependent port, you will not know how to write it.  This and the other mod-makefiles effort would be entirely useable via synth or portmaster or whatever port building automation tool you wish.
