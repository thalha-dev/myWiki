# DUNST

#### command

* ```notify-send "TITLE" "MESSAGE"```
* ```notify-send "TITLE" "MESSAGE" -u normal``` , set urngency to normal
* ```notify-send "TITLE" "MESSAGE" -u critical``` , set urngency to critical

* ```dunstify "TITLE" "MESSAGE"``` , another command with more feaature
* ```dunstify "TITLE" "MESSAGE -i ~/.config/myIcons/moon.png"``` , set the icon to use
* ```dunstify "TITLE" "MESSAGE -t <num>"``` , set the timeout count
* ```dunstify "TITLE" "MESSAGE -r <idNum>"``` , set the id num so never stack up

* ```dunstctl <command>```,to control the notification.
* ```dunstctl close```,to close
* ```dunstctl close-all```,to close all
* ```dunstctl history-pop```,to get missed notification.

