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

Building
=========

This module has been successfully built against InspIRCd v2.0.5. It's likely
to build against other versions but this hasn't been verified.

Clone the latest version of InspIRCd from the repository

    git clone git://gitorious.org/inspircd/inspircd.git && pushd inspircd

Create a local branch and checkout into the new branch

    git checkout -b insp205 v2.0.5

Download the module

    wget -O src/modules/extra/m_chatlog.cpp https://raw.github.com/joshenders/inspircd-m_chatlog/master/m_chatlog.cpp

Enable the module

    ./configure --enable-extras=m_chatlog.cpp

Configure

    ./configure

Build and install

    make && make install

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
