# ILFT - Interactive Linux File Tools

![GitHub](https://img.shields.io/github/license/MatMasIt/ilftools)

Collection of tools for interactive and metadata-friendly directory and file management



* **Ils**

  *Interactive ls*

  Ls, with pretty tables, dir overviews, permissions and much more

  The author data is fetched from ``{DIR}/.ilft`` as saved by **Imkdir**

  Example

  

  ![img](https://i.imgur.com/CbWOHxA.png)

  ![img](https://i.imgur.com/K7YO5YP.png)

  ```
  usage: Ils [-h] [--by-size-descending] [--by-size-ascending] [--by-adate-descending]
             [--by-adate-ascending] [--by-cdate-descending] [--by-cdate-ascending]
             [--by-mdate-descending] [--by-mdate-ascending] [--by-name-descending]
             [--by-name-ascending] [--group] [--markdown] [--show-author-info]
             dir
  
  Improved ls
  
  positional arguments:
    dir                   DIRECTORY
  
  optional arguments:
    -h, --help            show this help message and exit
    --by-size-descending, -sd
                          Sort by descending size
    --by-size-ascending, -sa
                          Sort by ascending size
    --by-adate-descending, -ldd
                          Sort by descending access date
    --by-adate-ascending, -lda
                          Sort by ascending access date
    --by-cdate-descending, -cdd
                          Sort by descending creation date
    --by-cdate-ascending, -cda
                          Sort by ascending creation date
    --by-mdate-descending, -mdd
                          Sort by descending edit date
    --by-mdate-ascending, -mda
                          Sort by ascending edit date
    --by-name-descending, -nd
                          Sort by descending name
    --by-name-ascending, -na
                          Sort by ascending name (Default)
    --group, -g           Group by type (directories, files, symlinks)
    --markdown, -md       Print markdown table
    --show-author-info, -a
                          Show author information about the directory (folders created with
                          Imkdir)
                      
  ```
  
* **Ilmkdir**

  *Interactive mkdir*

  Mkdir with author data

  On the first run, it saved personal information in ``~/.config/ilftools/author``  through a guided procedure

  When a directory is created through this tool, data is saved in ``{DIR}/.ilft`` 
  
  ```
  usage: Imkdir [-h] [--version] [--mode mode] [--parents] [--verbose] [-Z]
                [--context context] [--emulate] [--anonymous]
                dir [dir ...]
  
  Improved mkdir
  
  positional arguments:
    dir                   DIRECTORY(ies)
  
  optional arguments:
    -h, --help            show this help message and exit
    --version             show program's version number and exit
    --mode mode, -m mode  set file mode (as in chmod), not a=rwx - umask
    --parents, -p         no error if existing, make parent directories as needed
    --verbose, -v         print a message for each created directory
    -Z                    set SELinux security context of each created directory to the
                          default type
    --context context     like -Z, or if CTX is specified then set the SELinux or SMACK
                          security context to CTX
    --emulate, -e         Emulate mkdir directly, no additional features
    --anonymous, -a       Don't add personal info to the directories
  ```
  
  
