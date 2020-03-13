# Enhancements for SMB2 support in NMAP Script Engine

## Why

The smb2 implementation that is part of NMAP lacks support for parsing
`NEGOTIATE_CONTEXT` structures that can be used to determine hosts
that might be vulnerable to CVE-2020-0796. The code in this repository
adds that functionality.

## Usage

The modified `smb2.lua` library and the modified
`smb2-capabilities.nse` sript are intended to be used with NMAP 7.70.

Copy or symlink `smb2.lua` to `~/.nmap/nselib/` and use the NSE script
on a host:

    nmap --script=`pwd`/smb2-capabilities.nse $IP

## Author

Hilko Bengen <<bengen@hilluzination.de>>
