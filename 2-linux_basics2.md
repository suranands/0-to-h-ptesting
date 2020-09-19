# Linux Basics 2

## Today 12 Sep 2020

- `adduser bob` command adds a new user called bob to Kali
- The last lines of `/etc/passwd` file usually shows the users we added, for example bob in the above case. Navigating to this file and reading it can be done with several command, e.g. `cat` or `less`
- `cat /etc/shadow` command shows a shadow file of the password file, but this file contains a *hash* next to root, which should be accessible only the root, and nobody else. You can also see the hashes for the users created on this system, like for bob in the above example.
- There are 'unshadowing' tools that can decrypt hashes to log in as root. Cyber Mentor made a video on this, how to crack hashes.
- Whenever you see a message like, `bob: user not in the sudoers list. This will be reported.`, that means a log is created in the `/var/log/auth.log` that bob tried to access something he should not have. In thoery, an admin can take action on bob based on this. But in reality, there would be 101 reasons why bob did this, and could be easily justified.
