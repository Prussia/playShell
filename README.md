# playShell
Linux Shell Script Learning


1. grant user <user> to access docker

   ```
   usermod -a -G docker <user>
   ```
2. make sh executable
   
   ```
   $ chmod +x *.sh
   ```
3. Show group permission on current path

    ```
    $ ls -ld $(pwd)
    ```
  
4. 
    ```
    $ ls -ld some_dir
      drwxrwxr-x 2 alex consult 4096 Feb 20 10:10 some_dir/
                    ^     ^
                    |     |_____ directory's group
                    |___________ directory's owner
    ```

5.

6.

7.

8.
