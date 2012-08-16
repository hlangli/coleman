coleman
=======

Coleman Git Repository

Coleman is yet another attempt at a Maven continuous integration server, but this one differs in that it doesn't need any configuration!  Any.

This means that you can get continuous integration in a matter of seconds - just download, uncompress, and run!

It currently only works with Subversion checkouts, but support for other versioning systems can easily be added (see coleman-scm-change script).

How to use:
===========

$ cd &lt;maven-projects-parent-dir&gt; && &lt;coleman-dir&gt;/bin/coleman &lt;check-interval-in-seconds&gt;

If a build fails, and it has one or more /project/developers/developer nodes in the pom, it will send an email to each developer with the log-output from coleman.

If there's one or more projects under the root-folder that you don't want coleman to deal with, just put an empty file (touch) in that folder with the name .coleman-ignore

Technology
==========

Coleman is written mostly in Bash shell-script and Jash; a Java "interpretor" (it doesn't interpret anything, just wraps the contents in a main-method, sets up the classpath, and runs the darn thing).  The Jash-interpretor is included in coleman, and coleman will set the interpretor-declaration in all coleman-jash-scripts if it cannot find jash in /usr/bin (default).

The name
========

There's a tradition that Maven continuous integration projects should have butler-like names.  For those who didn't know or whom it may concern (I can't think of any reason), Coleman is the name of the butler in the movie "Trading Places" from 1983.

