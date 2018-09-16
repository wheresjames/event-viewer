# event-viewer

Command line event log viewer.

[Screen Shot](https://raw.githubusercontent.com/wheresjames/event-viewer/master/docs/imgs/view-kmsg.png)

This python script `evv` will allow you to graphically navigate log files.

## Keyboard

* LEFT = Scroll back in time
* RIGHT = Scroll forward in time
* UP = Zoom in
* Down = Zoom out

* s = Scroll automatically
* l = Change number of lines per record
* q / esc = Quit


##Examples:

* Navigate kernel messages

`sudo evv -f /dev/kmsg -d kmsg`

* Navigate syslog messages

`sudo evv -f /var/log/syslog`

* View data from stdin

`echo "Hello World!" | evv -f -`


