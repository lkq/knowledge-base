# Linux Shell Script Cheat Sheet

## <strong>IF</strong>
* File Exists / Not Exists
```
# file exists
if [ -f /tmp/foo.txt ]
# file not exists
if [ ! -f /tmp/foo.txt ]
# directory exists
if [ -d /tmp ]
```

* String Null / Not Null
```
# string not null
if [ -z "" ]
# string null
if [ -n "" ]
```