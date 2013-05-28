#!/bin/bash

PUUSH_API_KEY=""

if [ -z "$PUUSH_API_KEY" ]
then
  echo "Set the variable PUUSH_API_KEY in $0 or with 'export PUUSH_API_KEY=\"apiKeyHere\""
  exit
elif ! [ -r "$1" ]
then
  echo "Specify a file to be uploaded"
  exit
fi

curl "https://puush.me/api/up" -# -F "k=$PUUSH_API_KEY" -F "z=poop" -F "f=@$1" | sed -E 's/^.+,(.+),.+,.+$/\1\n/'
