# Cap
nmap -sS -T4 -A 10.10.10.245
21/tcp open  ftp     vsftpd 3.0.3
22/tcp open  ssh     OpenSSH 8.2p1 Ubuntu 4ubuntu0.2 (Ubuntu Linux; protocol 2.0)
80/tcp open  http    gunicorn


username called Nathan

wireshark file
1	0.000000	10.10.17.198	10.10.10.245	TCP	68	55142 → 80 [ACK] Seq=1 Ack=1 Win=502 Len=0 TSval=1510724671 TSecr=733458534
2	0.000127	10.10.17.198	10.10.10.245	TCP	68	55140 → 80 [ACK] Seq=1 Ack=1 Win=502 Len=0 TSval=1510724671 TSecr=733457614
3	0.658065	10.10.17.198	10.10.10.245	TCP	68	[TCP Dup ACK 1#1] 55142 → 80 [ACK] Seq=1 Ack=1 Win=502 Len=0 TSval=1510725044 TSecr=733458534

## Hints

For user, I would find a tool good for reading pcap files. There's a tool named after a fish (that has an entire week dedicated to it) that I found useful for this.

User: Count down from 2 and it will find you. Parse what you find.

pcab files 

found on the 0.pcab

36	4.126500	192.168.196.1	192.168.196.16	FTP	69	Request: USER nathan

40	5.424998	192.168.196.1	192.168.196.16	FTP	78	Request: PASS Buck3tH4TF0RM3!

open ftp connection
found the user flage
ftp> get user.txt

try the same credintials in ssh

ls

═════════╣ Finding emails inside logs (limit 70)
      2 giometti@linux.it
      2 dm-devel@redhat.com

/tmp/LinEnum.sh:    echo -e "\e[00;33m[-] htpasswd found - could contain passwords:\e[00m\n$htpasswd"
/tmp/LinEnum.sh:  echo -e "\e[00;31m[-] Contents of /etc/passwd:\e[00m\n$readpasswd" 
/tmp/LinEnum.sh:  echo -e "\e[00;31m[-] Password and storage information:\e[00m\n$logindefs" 
/tmp/LinEnum.sh:  echo -e "\e[00;33m[+] We can connect to Postgres DB 'template0' as user 'postgres' with no password!:\e[00m\n$postcon1" 
/tmp/LinEnum.sh:  echo -e "\e[00;33m[+] We can connect to Postgres DB 'template0' as user 'psql' with no password!:\e[00m\n$postcon2" 
/tmp/LinEnum.sh:  echo -e "\e[00;33m[+] We can connect to Postgres DB 'template1' as user 'postgres' with no password!:\e[00m\n$postcon11" 
/tmp/LinEnum.sh:  echo -e "\e[00;33m[+] We can connect to Postgres DB 'template1' as user 'psql' with no password!:\e[00m\n$postcon22" 
