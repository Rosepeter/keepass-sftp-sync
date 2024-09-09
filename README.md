
ARCHIVED 05/20/2024:
====================
As of the above date, I'm archiving this repo.  I no longer use this plugin myself, and as such do not have an easy way to test or maintain it.
Furthermore, the upstream project that this relies on SSH.NET does not seem to be interested in supporting non-Windows platforms, meanwhile the list of features and bugfixes continues
and I have no way to keep a unified codebase for all OS's.  I've attempted to patch upstream library to support the features I need that aren't compatible, but have no succeeded.  
Another issue is that at one point we supplied Putty support, but had to drop that because upstream patches were rejected.  In all this is becoming too painful for me to maintain
and I lack the time or interest to continue.  KeepassXC now supports KDBX v4 databases and has a built-in SSH agent.  I recommned people who want this functionality checkout that option.
If someone wants to take this project over, I'm open to the idea of transfering this repo, but I'm leery of someone of unknown reput hijacking it.  Feel free to open an issue to discuss.



Keepass SftpSync
================

This tool is based on (and primarily composed of) the work done by: Vitaly Burkut.
The original tool's source can be found here: https://sourceforge.net/projects/keepass-sftp-sync/

This version of the tool contains minor code clean-ups, and one major change.
The previous verions will timeout on a slow network connection, this version adds a 2 minute timeout, so even on an extremely slow network connection, you can still access your KeePass wallet.
In addition, this version is compiled against .NET 4.0.

I hope to continue development of this addon, as the original developer has not made any updates since 2016.

Connecting to your database through sftp can be set up with `Open URL...` menu option

Change Log
--------------
09.09.2024  2.4.x: Remove pageant support

26.10.2020  2.4.1: Minor Update to fix previous version bump mistake (This should stop you from getting alerts to update.)

27.09.2020  2.4: Explicitly close SSH session to prevent session hangs.

14.07.2020  2.3: Updated SSH.NET verion.  Added Pageant Support for Windows (Thanks to @kins-dev)

28.05.2020  2.2: Added SSH Private Key Support.

16.05.2020  2.1: Added configurable SSH connection timeout under advanced options, added update checking capabilities.

14.05.2020  2.0: Fixed some spelling errors, updated SSHNet Lib version, added extended timeout for connections.

27.12.2016  1.1: Add support scp, add keyboard authenticate, add check host key

24.12.2016  1.0: Support sftp protocol, for sync keepass db
