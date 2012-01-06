About
=====

The Channel Chat Logging module is a third-party InpsIRCd module that logs all
user messages as well as channel joins, parts, and quits. It logs with a type
of `m_chatlog` to make it easy to filter to a separate log file.

Credit
======

The original module was written by Daniel Rich <drich@employees.org> and forked
rather impatiently on github by Josh Enders <josh.enders@gmail.com>.

See: http://www.inspircd.org/forum/showthread.php?t=5592

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
