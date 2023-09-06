## DIRTY PIPE `CVE-2022-0847`

This is a kernel vulnerability that allows overwriting of data in
arbitrary read-only files, which can therefore lead to privilege escalation since an unprivileged 
process can write into a privileged process. All credits go to 🥇[Max Kellermann](https://dirtypipe.cm4all.com/) for finding the vulnerability and his good explanation/description of the vulnerability.

![profile](dirty_pipe.png)


#### 👻 IMPORTANT NOTICE

This proof of concept code is based on `Max Kellermann's` poc, that has been modified to explore some different 
ways on how this vulnerability can be used to gain higher privileges. The exploit code includes a check  to check if the kernel version is vulnerable and using the vulnerability to overwrite `/etc/passwd` file to gain root privileges. [exploit.c](dpipe.c)

### Usage

> You can download the already compiled binary or using `make` compile the binary locally and run it to gain `root`.
