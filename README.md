imapeval
========

IMAP folder evaluator

Description:
This perl script connects to an IMAP host with credentials you provide, and returns a report of the number of messages in and total size of each subfolder.  The report can be sorted by folder name, message count, or folder size, in ascending or descending order.  Folder sizes can be displayed in B, KB, MB, or GB.

Required non-standard libraries (install these and any dependencies):

    CPAN modules:
        Net::IMAP::Simple
        Email::Simple
        IO::Prompt

    Ubuntu/Debian packages:
        libnet-imap-simple-perl
        libemail-simple-perl
        libio-prompt-perl

Usage:
    imapeval [-h] [-u] [-p] [-f|-c|-z] [-a|-d] [-b|-k|-m|-g] [-v] [-h]

    Connection credentials will be prompted for if not provided on the command line
        --host, -i          IMAP hostname to connect to
        --user, -u          username for connection credentials
        --password, -p      password for connection credentials

    Sort selection options are mutually exclusive
        --sortfolder, -f    sort by folder name (default)
        --sortcount, -c     sort by count of messages in folder
        --sortsize, -z      sort by size of folder

    Sort direction options are mutually exclusive
        --ascending, -a     sort ascending (default)
        --descending, -d    sort descending

    Size formatting options are mutually exclusive
        --bytes, -b         display size in bytes
        --kilobytes, -k     display size in kilobytes
        --megabytes, -m     display size in megabytes (default)
        --gigabytes, -g     display size in gigabytes

        --verbose, -v       be a little more verbose
        --help, -h          display this help

Author:
Seth D. Galitzer <sethgali@gmail.com>
