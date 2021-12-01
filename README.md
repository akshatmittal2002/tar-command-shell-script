# TAR Command Shell Script
This `shell script` replicates all functionalities of `tar` command which is present in `LINUX Terminal`.<br>
***
To use the scipt, run this command in terminal:<br><br>
```bash
bash -f main.sh [options-of-tar] [archive-file] [files-to-be-archived]
```
where,<br>

`options-of-tar` : options to be given with `tar` command<br>
`archive-file` : file name of the archive file<br>
`files-to-be-archived` : all files separated by space to be included with `tar` command
***
<br>

## Available Options:
- `c` : create an archive
- `r` : append files at the rear end of an existing archive
- `t` : list table of contents
- `x` : extract individual contents
- `f` : file to be created within a file system
- `f-` : write/read from standard output/input
- `v` : verbose mode, give details of archive information
***
<br>

### Note:
1. As per actual `tar` command, exactly one of `-crxt` option should be given.<br>So, same is been implemented in my script as well.
2. All possible options for user are:
    - -cvf
    - -rvf
    - -tvf
    - -xvf
    - -cf
    - -rf
    - -tf
    - -xf<br>
3. Any other combination would display error message as in `tar` command.
4. Files created using some other means or by using inbuilt `tar` command can not be modified by my shell script.<br>Only the archives created using my script can be extracted/appended.
5. `MOST IMPORTANT` : My program handles archiving of only text files (i.e., `.txt` , `.sh` , `.c` , `.pl` etc.).<br>If user tries to archive other files like `.mp4`, then achive file would be created successfully but if user extracts that file, it will be corrupted.
