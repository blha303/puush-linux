puush-linux
===========

A Bash script for uploading files to puush.me from Linux. Many thanks to @Westie for his insights on puush's undocumented API :)

Using
-----

Copy 'puush' to /usr/bin. Use it with `puush file.name`. You'll need to set up an environment variable, PUUSH_API_KEY. You can do this per-session with `export PUUSH_API_KEY="apiKeyHere"`, or by putting that command in `~/.bashrc`.
