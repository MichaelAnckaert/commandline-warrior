# grep cheatsheet

## Basics
With grep you can search files for text:

`$ grep stuff file.txt`

The grep command follows the following pattern:
`grep [OPTIONS] PATTERN [FILE...]`

If there are no files specified, grep will read from STDIN. If you don't specify any files and use the *recursive* option `-r`, grep will search the current working directory.

## Options

There are plenty of options to specify to grep, check out `$ man grep` for the full rundown. Here are some of the most interesting options.

|Option|Description|
|--|--|
|`-i`|Case insensitive search|
|`-r`|Recursively search through files|

## Context

When grep finds a matching line in a file, it will print the matching line. This can get confusing because a single line often doesn't show you where you are in the file. 

By specifying a context paremeter you can add additional context to the grep out:

`grep -B 3 stuff file.txt`

The example above specifies the option `-B 3`, which tells grep to add 3 additional lines **b**efore the matching line. 

|Option|Description|
|--|--|
|`-A`|Show lines matching after|
|`-B`|Show lines matching before|
