squid-perl-hacks
================

Squid related Perl scripts

1. imap-auth.pl
===============

http://www.squid-cache.org/mail-archive/squid-users/201206/0058.html
Squid's basic auth helper for authentication against IMAP and IMAPS servers.

IMAP:
=====
imap-auth.pl imap://imap.myserver.com mymaildomain.com

IMAPS:
======
imap-auth.pl imaps://imap.google.com mymaildomain.com

maildomain argument is required to prevent users from authenticating with their other domain accounts
on the same server.

e.g.
Your domain, say mydomain.com, has it's mail hosted with google. You don't want users to authenticate
with some random gmail account.


This is the first attempt at creating any helper for squid.
report bugs to: codemarauder [at] gmail [dot] com

2. Dependencies
===============

Centos:
yum install cpan
yum -y install perl perl-Net-SSLeay openssl perl-IO-Tty 
yum install openssl-devel perl perl-Net-SSLeay perl-Crypt-SSLeay
yum isntall perl-Mail-IMAPClient

Ubuntu: 
apt-get install libauthen-simple-pam-perl  

All:
cpan install Mail::IMAPClient  
cpan Try::Tiny 
