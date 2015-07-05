puush-linux
===========

A Bash script for uploading files to puush.me from Linux. Many thanks to @Westie for his insights on puush's undocumented API :)

Update with `--showlink` by wessles.

Using
-----

* Get `curl` if you don't have it already. Most package managers have it as `curl` (apt-get install curl, yum install curl), or check this page: http://curl.haxx.se/download.html
* Get `zenity` as well.
* Copy the 'puush' script to /usr/local/bin, and use `chmod +x /usr/local/bin/puush` to make it runnable.
* Use it with `puush file.name`. You can also use the `--showlink` flag to open a window containing the puush link to the file after upload.

You'll need to set up an environment variable, PUUSH_API_KEY. You can do this per-session with `export PUUSH_API_KEY="apiKeyHere"`, or by putting that command in `~/.bashrc`.
