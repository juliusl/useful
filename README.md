# Julius's List of Useful Things He's Spent Time Figuring Out

## 1. Searching for a bunch of files on your disk and executing a command on them
In Windows, 
```
forfiles /s /m *.txt /c "cmd /c copy /v @path c:\dest\@file"
```
This bad boy will search recursively (starting in the directory you ar currently in) for all files that match *.txt and copy it to a directory under c:\dest. @path is the path to the file found and @file is the name of the file with extension. Got this from [http://ss64.com/nt/forfiles.html](http://ss64.com/nt/forfiles.html), but took a lot of tinkering to get it right. Could be used to do the super cool spy stuff, or even run as a script to auto backup your drives, or cleanup old files. Linux version might be: 
```
find / -name *.txt -exec "cp {} /home/dest/"
``` 
but I hadn't had a chance to test it.
