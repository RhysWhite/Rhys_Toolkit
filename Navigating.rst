Navigating the directory structure
===================================

Printing the current working directory
---------------------------------------

The full path of the current working directory will be printed to standard output if you use the `pwd` command. 
.. code-block::
$ pwd 
	
/Users/rhys


Showing the contents of a directory
---------------------------------------

The `ls` command will list the contents of a directory and print to the screen as standard output.
```
$ ls /Users/rhys
Applications  Movies     bin         Music      Desktop   Downloads
Dropbox       Pictures	 miniconda2  Documents	Public    miniconda3
```

To list all files with detailed information, use:
```
$ ls -l
```

To list all files in a directory and order by time, use:
```
ls -l -t
```

To list the top 3 lines (2 files and the total)
```
ls -l -t | head -3
```

To list the first 2 lines of files (skipping the size line)
```
ls -l -t | tail -n +2 | head -2
```

To list the unique files using the first 7 characters of file names
```
ls -1 | cut -c1-7 | sort -u
```

To list and use cut to split the text by "_" and takes the first field of each file name
```
ls -1 | cut -f1 -d"_" | sort -u
```

To list files in directory and count lines
```
ls -1 | wc -l
```
	
To list lines in directory and count characters	
```
while read f ; do echo $f | wc ; done < ${FILE}
```

Making a new directory
---------------------------------------

The `mkdir` command will create a directory(s)
The `rmdir` command will delete a directory(s)
```
$ cd /home/<user_ID>
$ mkdir week1
$ mkdir week1/seqs
$ cd week1
```

Changing directories
The `cd` command will allow you to move around your directories

To move into your directory, use:
```
$ cd week1 
```
To move up one level in the directory tree, use:
```
$ cd ../ 
```
To move to the `week1/seqs` directory, use
```
$ pwd
/Users/<user_ID>

$ ls 
week1

$ cd week1/seqs 
```
To return to your home directory, use:
```
$ ls
/Users/<user_ID>/week1/seqs 

$ cd 

$ pwd
/Users/<user_ID>
```

Moving directories
---------------------------------------

To move files (can also use for renaming), use:
```
$ mv <Path/To/File/filename> <destination>
```
A similar command can be used for copying files:
```
$ cp <Path/To/File/filename> <destination>
```
