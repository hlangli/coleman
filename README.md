coleman
=======

Coleman Git Repository

Coleman is yet another attempt at a Maven Continuous Integration server, but this one differs in that it practically doesn't need any configuration!

It currently only works with Subversion checkouts, but support for other versioning systems can easily be added (see coleman-scm-change script).

How to use:
===========

$ cd <maven-projects-parent-dir>
$ <coleman-dir>/bin/coleman <check-interval-in-seconds>

If a build fails, and it has one or more /project/developers/developer nodes in the pom, it will send an email to each developer with the log-output from coleman.

Is that simple enough?

