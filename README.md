# OS X Self Destruct
==================

Version: 0.9

Securely destroys files or directories on a delay based on their OS X "Tag."

Available Tags: 1 Minute, 1 Hour, 1 Day, 1 Week, 1 Month, 1 Year

For example, if a file is tagged with "1 Week" then it will be deleted at the time exactly one week from the last time the file was modified.

This allows you to put a self-destruct on files you would otherwise forget about, leaving your system crowded with junk.

#### WARNING: If you tag a file that was modified in the past, the time-to-delete will be in the past and it may be deleted on the next run of Self Destruct. This script uses *srm* (Secure Remove), which will not only erase the file(s), but will use a multi-pass erase which render the files un-recoverable and un-traceable.

### HELP

```bash
./self-destruct.sh --help
```

#### INSTALLATION

To install Self Destruct, copy this file to a permanent location and put the following entry in your crontab (making sure to point to the path you place the file in):

```bash
* * * * * /path/to/self-destruct.sh --run
```

This will run Self Destruct every minute.

#### USAGE

Once you have installed the cron process and it is actively working, you can start using self destruct immediately.

*Open Tags Option*

To get to the Tags area, right click on the file(s) you wish to tag and select "Tags..."

![Open Tags Menu](http://scottmw.com/wp-content/uploads/2014/09/tags-menu.png)

*Select Desired Tag*

Assign one of the predetermined tags to the file (spelling/spacing are important, but the character case does not matter):

- 1 Minute
- 1 Hour
- 1 Day
- 1 Week
- 1 Year

![Select Desired Tag](http://scottmw.com/wp-content/uploads/2014/09/tags-assign.png)

*Verify Tag*

You can verify the tag was placed on the file(s) by doing a simple search (e.g. "1 Day") and selecting the tags option.

![Search for Tag](http://scottmw.com/wp-content/uploads/2014/09/tags-search.png)

Once you've searched for the tag, you can see any files slated for self destruct.

![Verify Tag by Search](http://scottmw.com/wp-content/uploads/2014/09/1day-delete.png)

And now we wait.

### RUNNING MANUALLY

If you want to 

```bash
chmod +x self-destruct.sh
./self-destruct.sh --run
```


### Disclaimer

Although I have used this for months without a problem, using this means you are doing so at your own risk.

Copyright &copy; 2014 [Scott Weaver](http://scottmw.com/)