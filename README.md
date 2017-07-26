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

5. [Systemd](https://coreos.com/os/docs/latest/getting-started-with-systemd.html)

   systemd is an init system that provides many powerful features for starting, stopping, and managing processes. Within Container Linux, you will almost exclusively use systemd to manage the lifecycle of your Docker containers.

   /etc/systemd/system
   
[Unit]
Description=MyApp
After=docker.service
Requires=docker.service

[Service]
TimeoutStartSec=0
ExecStartPre=-/usr/bin/docker kill busybox1
ExecStartPre=-/usr/bin/docker rm busybox1
ExecStartPre=/usr/bin/docker pull busybox
ExecStart=/usr/bin/docker run --name busybox1 busybox /bin/sh -c "trap 'exit 0' INT TERM; while true; do echo Hello World; sleep 1; done"

[Install]
WantedBy=multi-user.target

6.

7.

8.
