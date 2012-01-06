About
=====

The Channel Chat Logging module is a third-party InpsIRCd module that logs all
user messages as well as channel joins, parts, and quits. It logs with a type
of `m_chatlog` to make it easy to filter to a separate log file.

Credit
======

The original module was written by Daniel Rich <drich@employees.org> and forked
on github by Josh Enders <josh.enders@gmail.com>.

See: http://www.inspircd.org/forum/showthread.php?t=5592

Compiling
=========

This module has been successfully built against InspIRCd v2.0.5. It's likely
to build against other versions but this hasn't been verified.

Check out the latest version of InspIRCd from gitorious

    git clone git://gitorious.org/inspircd/inspircd.git

Create a local branch for the `v2.0.5` tag and start tracking it

    git checkout -b v2.0.5 origin/v2.0.5

Copy the module to the `inspircd/src/modules/extra/` directory

    cp m_chatlog.cpp inspircd/src/modules/extra/

Enable the module

    ./configure --enable-extras=m_chatlog.cpp

Configure

    ./configure

Compile

    make

Configuration
=============

The following lines should be appended to `/etc/inspircd/modules.conf`

    #-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#-#
    # Chat log module: Logs all chats to the ircd log at default loglevel.
    <module name="m_chatlog.so">
    
    #-#-#-#-#-#-#-#-#-# CHATLOG CONFIGURATION #-#-#-#-#-#-#-#-#-#-#-#-#-#
    # There may be certain nicks that you do not want logged for security
    # reasons. Exceptions can be added below.
    #<chatlog exception="nickserv">
    #<chatlog exception="chanserv">
