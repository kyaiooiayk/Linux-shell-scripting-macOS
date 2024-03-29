
# Linux commands

## `alias`
Create shortcuts for your most frequently used command by creating aliases. It requires a
shortcut name and command as a string. You will print “I love KDnuggets” by typing love in the terminal.
`$ alias love="echo 'I love GitHub!'"`
***

## `source` vs `export`
- `source some_script.sh`, or the POSIX-compliant equivalent, `. some_script.sh`, brings variables **in** from other scripts. Something similar is done in python with `import some_module` in Python, or `#include <some_header_file.h>` in C or C++.
- `export my_var="something"` pushes variables **out** to other scripts/processes which are called/started from the current script/process. Using export some_var="something" is kind of like setting that variable locally, so it is available for the rest of the current script or process, and then also passing it in to any and all sub-scripts or processes you may call from this point onward.
***

## `chmod`
- Give a bash file (*sh.) persmission to be run: `$ chmod +x filename.sh`
***

## `curl`
- cURL stands for client URL.
- The curl command transfers data to or from a network server, using one of the supported protocols (HTTP, HTTPS, FTP, FTPS, SCP, SFTP, TFTP, DICT, TELNET, LDAP or FILE). 
- It is designed to work without user interaction, so it is ideal for use in a shell script. 
- The software offers proxy support, user authentication, FTP uploading, HTTP posting, SSL connections, cookies, file transfer resume, metalink, and other features. 
- `curl [options] [URL...]`
- Checks the version of cURL you have installed on your system: `curl --version`
***

## `echo`
- Print text on console: `$ echo "Hello world!"`
***

## `grep`
- It stands for "Global Regular Expression Print".
- It is used to find data within the file. 
- Given a text pattern, find all the lines containing that pattern: `$ grep -i "vir" file.csv`
***

## `head` and `tail`
- Print the first 10 lines of a document: `head -10 file.txt` 
- Print the last 10 lines of a document: `tail -10 file.txt` 
- Select the first 10 lines of a document and write them in a new file: `head -10 file.txt > first_10_lines_file.txt` 
***

## `history`
- Print the last 1,000 command line history: `>>history`
- Search in the command history for command lines that contain the word `docker`: `>>history | grep docker`
***

## `man`
Learn about any Linux commands or tools by using the man command and the tool name. The man stands for manual: `$ man echo`
***

## `which` and `type`
- `which` shows the full path of (shell) commands. Its output is different based on different systems.
```shell
$ type cd
cd is a shell builtin
```
- `type` display information about command type on Linux. We have 4 command types:
  - Built-in Shell Commands
  - Shell Functions
  - Command Alias
  - excutable Programs 
```shell
$ which cd
cd is a shell builtin
cd is /usr/bin/cd
cd is /bin/cd
```
***

## Folders
- List only directories: `>>!ls -d */`
- List all files in a folder in a long list format: `>>ls -l`
- Count all the elements inside a folder: `ls ./local_path | wc -l`
***

## `touch`
- The touch command is a standard command used in UNIX/Linux operating system which is used to create, change and modify timestamps of a file. Basically, there are two different commands to create a file in the Linux system which is as follows:
  - `cat` command: it is used to create the file with content.
  - `touch` command: it is used to create a file without any content. The file created using touch command is empty. This command can be used when the user doesn’t have data to store at the time of file creation.
***

## `screen`
- To start a screen session: `screen`
- To detach the session while keeping what you sent in the background: `ctrl+a+d`
- To resume what you were doing: `screen -r <process ID>	`. If it throws an error try: `screen -rd <process ID>	`
- List all the screen sessionts: `screen -ls`
- Kill the process with: `skill <pid>`
***

## `fg` & `bg`
- The `fg` command, short for the `foreground`, is a command that moves a background process on your current Linux shell (meaning the foreground). 
- This `bg` command, short for `background`, that sends a process running in the foreground (meaning the current Linux shell) to the background.
***

## `ps`
- `ps` command is used to list the currently running processes and their PIDs along with some other information depends on different options.
- Get the pid of a process if you know the applciation name: `$ ps aux | grep 'freemind'`
***

## `wc`
- Use wc to get information about word count, character count, and the number of lines: `$ wc file.csv`
-  Count only the number of line in the document: `$ wc -l file.csv`
***

## `wget`
- Wget is a networking command-line tool that lets you download files and interact with REST APIs. It supports the HTTP , HTTPS , FTP , and FTPS internet protocols. Wget can deal with unstable and slow network connections. In the event of a download failure, Wget keeps trying until the entire file has been retrieved.
- `wget [options] [URL...]`
***

## References
- https://github.com/jpicerno1/the-art-of-command-line/blob/master/README.md
- https://www.kdnuggets.com/publications/sheets/Linux_for_Data_Science_Cheatsheet_KDnuggets.pdf
- [`curl`](https://www.computerhope.com/unix/curl.htm) 
- [`which` and `type`](https://unix.stackexchange.com/questions/476951/what-differences-between-type-cd-and-which-cd-commands-in-linux/476955)
- [`wget`](https://www.digitalocean.com/community/tutorials/how-to-use-wget-to-download-files-and-interact-with-rest-apis)
- [`sourcw` vs. `export`](https://stackoverflow.com/questions/15474650/unix-what-is-the-difference-between-source-and-export)
***
