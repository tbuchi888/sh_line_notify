# sh_line_notify
## Summary
LINE Engineers' Blog [コマンドラインから LINE にメッセージを送れる LINE Notify](http://developers.linecorp.com/blog/ja/?p=3784)

## Usage
```
sh ./line_notify.sh ACCESS_TOKEN "foobar"
```

## Shell Script
``` line_notify.sh 
#!/bin/sh

ACCESS_TOKEN=$1
MSG=$2

curl -X POST -H "Authorization: Bearer $ACCESS_TOKEN" -F "message=$MSG" https://notify-api.line.me/api/notify
```
