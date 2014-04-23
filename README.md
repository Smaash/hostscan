hostscan 0.2
============

Hostscan is a php tool which allows you to scan specific range of hosts, mostly for information gathering
and testing for weak passwords. I guess it's a pentest tool, i'd created it to automate some tests that i
often do. Since it's PHP, it works quite slowly compared to client-side soft.

How it works?
 - You need to provide range of ip's (e.g. 127.0.0.1 - 127.0.0.10); program will perform operations on
 each address separately, basing on selected options, then it will print out the response.
 - By default, program will only check open ports, print http response headers, test for HTTP methods and
 check FTP for anonymous login.
 - If 'SSH/IMAP/DB's' are checked, program will try to bruteforce SSH,IMAP,MySQL,PostgreSQL & MsSQL using array of
 passwords and users defined on the beggining of script. Notice, that it will try to login as user with grand permissions
 (e.g. root, postgres), although you're able to edit it.
 - If 'FTP User' is set, program will also try to bruteforce FTP with specific user using mentioned passwords array.
 By default it's not, and it will only test for anonymous login.
 - If 'Deep Scan' is set, program will perform all aforementioned operations. Further, it will use nmap  with specific 
 parameters you're able to edit, also, the traceroute scan will be performed and displayed - just like nmap. Deep Scan
 also gather some useful informations about a website (if it's running), such as interesting files/folders and www title.
 - ?url=website.com for quick IP address of specific website.

 ...so - what it does it do? Nmap, traceroute, port scan, ftp anonymous login, ftp/ssh/imap/mysql/pgsql/mssql bruteforce, http (website) info gathering, 
 
 Crawler accepts as a parameter array of files and folders that you can manually edit, just like others options.
 
Some screens:
 - http://i.imgur.com/uw3qhaZ.png
 - http://i.imgur.com/JKgzJ0T.png
 - http://i.imgur.com/Upn25IP.png
 - http://i.imgur.com/nhtSW7L.png

TODO:
 - Website vulnerability scanning? (OWASP top ten)
 - Output?
 - Dunno yet.

Changelog 0.2:
 - Improved code.
 
Requirements (php5):
 - php5-mysql - for mysql connections
 - php5-pgsql - for postgresql connections
 - libssh2-php - for ssh connections
 - php5-sybase - for mssql connections
 - php5-imap - for imap connections


Any ideas? Feel free to contact me. 
