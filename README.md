# Linux Lab – Steganography with Steghide
## Objective

The objective of this script is to block incoming network traffic from a list of specified IP addresses using the iptables firewall in Linux. It automates the process of applying IP-based traffic restrictions for network security purposes.

### Job Skills Learned

- Linux System Administration
- Managing firewall rules using iptables.
- Bash Shell Scripting
- Using loops and conditional commands.
- Network Security and Access Control
- Automation and Efficiency


### Tools Used

- Linux Terminal Command Line Interface (CLI)
- Bash Shell
- iptables (Firewall)
- Networking Commands: ping, ifconfig
- VMware Tools: Linux VM

*Ref: Diagram:



### STEPS

STEGANOGRAPHY
 
# Installing steghide
`apt update && apt install steghide`
![image](https://github.com/user-attachments/assets/141308a1-5440-4ac4-9997-082f9bb1345f)

 
 
# Embedding a secret file into a cover file
`steghide embed -ef secret.txt -cf cat.jpg`
![image](https://github.com/user-attachments/assets/563c364e-9fa9-472f-91f2-fd530523b866)
 
 
# Getting info about a cover/stego file
`steghide info cat.jpg 
"cat.jpg":
  format: jpeg
  capacity: 47.5 KB
Try to get information about embedded data ? (y/n) n`
 ![image](https://github.com/user-attachments/assets/e0f146a8-03f4-404a-b9fa-b11424ac148a)

 
# Extracting the secret file from the stego file
`steghide extract -sf cat.jpg 
Enter passphrase: 
wrote extracted data to "secret.txt".`
![image](https://github.com/user-attachments/assets/86025db5-7377-4b05-a3fa-79bfc6166961)
 
