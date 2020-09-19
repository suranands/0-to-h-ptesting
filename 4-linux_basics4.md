# Linux Basics 4

## Today 13 Sep 2020

With the example below, I just learned something weird. I ran these commands on Kali VM, copied them and pasted here on KeepNote which is running on Windows, not in the VM. Didn't know this before, cool!

Anyway, just read through the commands, mostly self-explanatory.

```
root@kali:~# cd Documents/
root@kali:~/Documents# ls
root@kali:~/Documents# echo "hello" > hello.txt
root@kali:~/Documents# ls
hello.txt
root@kali:~/Documents# cat hello.txt
hello
root@kali:~/Documents# echo "hello again" > hello.txt
root@kali:~/Documents# cat hello.txt
hello again
root@kali:~/Documents# #Oops, we overwrote the file, so be careful.
root@kali:~/Documents# echo "hello again again" >> hello.txt
root@kali:~/Documents# cat hello.txt
hello again
hello again again
root@kali:~/Documents# #There you go, now you appended to the text, rather than overwriting.
root@kali:~/Documents# rm hello.txt
root@kali:~/Documents# ls
root@kali:~/Documents# touch hello2.txt
root@kali:~/Documents# ls
hello2.txt
root@kali:~/Documents# nano hello3.txt
root@kali:~/Documents# ls
hello2.txt  hello3.txt
root@kali:~/Documents# # To exit out of nano, use ctrl+x, say Y for yes, and hit enter!
root@kali:~/Documents#
```
