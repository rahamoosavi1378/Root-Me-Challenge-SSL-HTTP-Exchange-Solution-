
# Root-Me Challenge: SSL-HTTP Exchange \[Solution\]

**Challenge Link**: [SSL-HTTP Exchange](https://www.root-me.org/en/Challenges/Network/SSL-HTTP-exchange)

## Challenge Background
The challenge provides a clue:  
`"google is your friend : inurl:server.pem..."`  
suggesting we should search for a `server.pem` file using this Google dork.  

However, since this challenge was created in 2010 (and it's now 2025), the search results no longer return relevant files. After investigating solved write-ups, I found some archived links containing the necessary files.

Additionally, Wireshark's interface has changed over time, which affects the solution approach.

## Solution Approaches
*(I'll avoid spoilers so you can enjoy solving it yourself!)*

### Method 1: Using `ssldump`
```sh
ssldump -dq -r [fileName].pcap -k [fileName].pem
```
**Note**: Ensure `ssldump` is installed on your system.

### Method 2: Using Wireshark (Tested on Version 4.4.5)
1. Download the challenge file and open it in Wireshark.
2. Obtain the private key file (you can use the links/files I’ve provided below).
3. Configure Wireshark:  
   - Go to `Edit > Preferences... > Protocols > TLS`  
   - Under `(Pre)-Master-Secret log filename`, load the private key.  
  **Screenshot**:  
  ![Wireshark TLS Configuration](~/tmp/CTF/rootme/Challenges/Network/SSL-HTTP-exchange/wireshark-ssl-master-secret.png)  


4. Right-click on a `TLSv1` protocol row and select:  
   - `Follow > TLS Stream`  
   - Or use the shortcut: `Ctrl + Alt + Shift + S`  

---

## Related Files & Links
- [Link 1](URL)  
- [Link 2](URL)  
- [Link 3](URL)  
- [Link 4](URL)  

---

**Happy Hacking!** 🔐  

