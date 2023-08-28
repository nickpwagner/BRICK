___
# LINUX
Links: [[Operating Systems]]
Status: #🌳 
Tags: [[byobu]]
<!--- Created on: 2023.08.19, 18:49 --->

- open-source operating system kernel
- foundation for various Linux distributions (distros), such as Ubuntu, Fedora, and CentOS
- kernel + distribution = operating system (stable, secure, flexible)
- widely used in servers, supercomputers, embedded systems, and as an alternative desktop OS

___

| What                              | How                                                                                                                  | 
| --------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| Get Linux Version                 | `cat /etc/issue `                                                                                                    |
| Return current path               | `pwd`                                                                                                                |
| Return current directory          | `ls` **ll for details**                                                                                              |
| Update library                    | `sudo apt-get update`                                                                                                |
| Update package                    | `sudo apt-get upgrade`                                                                                               |
| Install package                   | `sudo apt-get install`                                                                                               |
| Workstation neu starten           | `sudo shutdown`                                                                                                      |
| Run shell script                  | `bash <pname>.sh`                                                                                                    |
| Install file                      | `cd location<br><br>sudo dpkg -i filename  `                                                                         |
| Kill process                      | `ps aux \| grep <program_name>chrome`<br>`kill process_id` **specific**  <br>`killall  process_name` **all**         |
| Change file type to executable    | `chmod +x …`                                                                                                         |
| Pfad von gesuchter Datei ausgeben | `realpath -s <file.txt>`                                                                                             |
| Compile Makefile                  | `make -f filename `                                                                                                  |
| VPN connection starten            | `osd-vpn-connect`                                                                                                    |
| Log into remote                   | `ssh user@server:/remote_path`                                                                                       |
| Copy from local to remote         | `scp -r local_path user@server:/remote_path`                                                                         |
| Copy from remote to local         | `scp -r user@server:/remote_path local_path`                                                                         |
| Wenn VM neu aufgesetzt            | `sudo apt-get update`<br>`sudo apt-get upgrade`<br>`sudo apt install build-essential dkms linux-headers-$(uname -r)` |
