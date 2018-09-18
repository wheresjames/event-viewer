# event-viewer

Command line event log viewer.

![Screen Shot](https://raw.githubusercontent.com/wheresjames/event-viewer/master/docs/imgs/view-kmsg.png)

This python script `evv` will allow you to graphically navigate log files.

## Keyboard

* LEFT = Scroll back in time
* RIGHT = Scroll forward in time
* UP = Zoom in
* Down = Zoom out

* s = Scroll automatically
* l = Change number of lines per record
* q / esc = Quit


## Examples:

* Navigate kernel messages

`sudo evv -i /dev/kmsg -I kmsg`

* Navigate syslog messages

`sudo evv -i /var/log/syslog`

* Navigate Apache web logs

`sudo evv -i /var/log/apache2/access.log -I www`

* View data from stdin

`echo "Hello World!" | evv -f -`


## Help

```
usage: evv [-h] [--inputfile INPUTFILE] [--inputformat INPUTFORMAT]
           [--inputbreak INPUTBREAK] [--inputfilter INPUTFILTER]
           [--outputfile OUTPUTFILE] [--outputformat OUTPUTFORMAT]
           [--timerange TIMERANGE] [--time TIME] [--refresh REFRESH]
           [--scroll SCROLL] [--lines LINES] [--maxmsgbuf MAXMSGBUF]
           [--maxfileread MAXFILEREAD] [--debug]

Event monitor.

optional arguments:
  -h, --help            show this help message and exit
  --inputfile INPUTFILE, -i INPUTFILE
                        Log file to parse
  --inputformat INPUTFORMAT, -I INPUTFORMAT
                        Input data format
  --inputbreak INPUTBREAK, -b INPUTBREAK
                        Line break
  --inputfilter INPUTFILTER, -f INPUTFILTER
                        Regex filter expression for input data
  --outputfile OUTPUTFILE, -o OUTPUTFILE
                        Append logs to output file
  --outputformat OUTPUTFORMAT, -O OUTPUTFORMAT
                        Output data format
  --timerange TIMERANGE, -r TIMERANGE
                        Time range
  --time TIME, -t TIME  Time start
  --refresh REFRESH, -R REFRESH
                        Data refresh interval in seconds, 0 for no refresh
  --scroll SCROLL, -s SCROLL
                        1-100, percentage of screen for auto scroll position,
                        0 = Do not auto scroll
  --lines LINES, -l LINES
                        Number of lines per timeline item, can be 1, 2, or 3
  --maxmsgbuf MAXMSGBUF, -m MAXMSGBUF
                        Maxium number of messages to queue
  --maxfileread MAXFILEREAD, -M MAXFILEREAD
                        Maxium number of bytes to read from a file, 0 for all
  --debug, -D           Show debug information
```
