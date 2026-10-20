# Hack The Box: Meow

First, start the machine and make sure you are connected to the correct network within Hack The Box.

![Task 1](images/meow/task1.png)

Open the bash terminal in Hack The Box. It is the green terminal in the middle.

![Terminal](images/meow/terminal.png)

![Task 2](images/meow/task2.png)

If you are not using Pwnbox, download the OpenVPN configuration and run it in a terminal. Leave that terminal open to keep the VPN connection active.

![Task 3](images/meow/task3.png)

Open a terminal and ping the Meow machine's IP address. In this example, the address is `10.129.96.15`. Press Ctrl+C after a few replies. This verifies that the VPN is working and your machine is on the correct network.

![Ping](images/meow/ping.png)

![Task 4](images/meow/task4.png)

Use Nmap to identify open ports and the services running on the target.

![Nmap](images/meow/nmap.png)

The scan shows Telnet open on TCP port 23. Telnet is a command-line protocol for remotely connecting to computers, but it does not encrypt traffic.

![Task 5](images/meow/task5.png)

Connect to the service by specifying the target address and port:

```sh
telnet 10.129.96.15 23
```

![Telnet](images/meow/telnet.png)

![Task 6](images/meow/task6.png)

At the login prompt, try default usernames such as `admin`, `administrator`, and `root`. For this machine, the username is `root` and the password can be left blank.

![Task 7](images/meow/task7.png)

After logging in, you have a root shell on the target.

![Root shell](images/meow/root-shell.png)

Use `ls` to list the files. The flag is in `flag.txt`; its value is redacted in accordance with the repository's spoiler policy.
