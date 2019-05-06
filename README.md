# FourAndSix-2.01
VulnHub boot to root walkthrough


# NETDISCOVER

Use netdiscover to find the IP of your VM. The target is 192.168.56.101

![Alt text](./netdiscover.png?raw=true)


# NMAP

Find open ports. NFS looks interesting and not much else is available.

![Alt text](./nmap.png?raw=true)


# TEST NFS

Use showmount to check for shares and then mount it.

![Alt text](./showmount3.png?raw=true)

![Alt text](./mnt4.png?raw=true)


# FILE

Suspicious file backup.zip is found. Decompressing requires password. Get 7z2john working from local binary or use github.

![Alt text](./john7z5.png?raw=true)


# HASH CRACK

Use rockyou to crack hash for zip password

![Alt text](./rockyou7.png?raw=true)


# EXTRACT

Gets pics and key pair

![Alt text](./extract9.png?raw=true)


# SSH TRY

Try to ssh but the key has a passphrase

![Alt text](./firstSSH10.png?raw=true)


# JOHN

Use ssh2john to get the hash from the ssh file.

![Alt text](./sshHash11.png?raw=true)


# CRACK HASH

The usual ssh key path doesn't work too well because the key is an OPENSSH format, not RSA. CLI command to validate password in a loop can try and crack this.


![Alt text](./sshkey13.png?raw=true)

![Alt text](./low-priv14.png?raw=true)

![Alt text](./foothold15.png?raw=true)

![Alt text](./doas19.png?raw=true)

![Alt text](./gtfo20.png?raw=true)

![Alt text](./less21.png?raw=true)

![Alt text](./less22.png?raw=true)

![Alt text](./rootshell24.png?raw=true)

![Alt text](./flag27.png?raw=true)


# Root

<pre>
\(*_*)
  ( (>
  /  \
</pre>

![Alt text](./rootshell24.png?raw=true)


# Flag

CTF completed.

![Alt text](./flag27.png?raw=true)
