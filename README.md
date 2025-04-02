# devalla-jwala-devalla-jwala-Week-3-Network-Scanning-Footprinting-and-Enumeration
Sapience Edu Connect Pvt Ltd -Internship task-3
Task3: 
## 1. Identify Target IP Range:  
a. Determine the target IP range for scanning 
Step 1: Gather Initial Information. 
Resolve the Domain to an IP Address 
Use a tool like nslookup or dig to resolve the domain name to an IP 
address. 
 
 
  nslookup testphp.vulnweb.com 
 
   dig testphp.vulnweb.com 
  
## 2 Perform Ping Scan:  
a. Toidentify active hosts within the target IP range. 
 
 Step1: ping testphp.vulnweb.com 

 
Nmap is a powerful network scanning tool that can perform a ping scan to 
identify active hosts. The command to perform a ping scan is: 
    
   nmap -sn 44.228.249.3 
 
 
## 3.Port Scanning: 
 a. Perform a comprehensive port scan on the identified active hosts to 
discover open ports 
 Step1: 
            Open your terminal and execute the following command to perform           
a comprehensive port scan on the identified active hosts: 
 
nmap -p- 44.228.249.3 
  
## 4.Service Enumeration: 
 a. Toidentify the version of services running on open ports.  
 
Step1: 
     Identify the version of services running on open ports. Nmap can 
help with this: 
 
    nmap -sn -v 44.228.249.3 
 
To determine the version of services running on open ports. 
 
## 5.Banner Grabbing: 
 a. Tograb banners from open ports to gather more information about 
the services. 
   
Step1: 
 Grab banners from open ports to gather more information about the 
services. Nmap can also be used for banner grabbing 
 
  nmap -sV --script banner 44.228.249.3 
  
## 6. OSFingerprinting:  
a. Toperform OS fingerprinting on the target machine. 

Step1: 
Perform OS fingerprinting on the target machine. Nmap can do this: 
 
nmap -sS -sU -O 44.228.249.3 
 
 
## 7.Footprinting:  
a. Use tools like whois, dig, and nslookup to gather additional 
information about the target network and domain. 
 
Step1: 
 
Use tools like whois, dig, and nslookup to gather additional information 
about the target network and domain.  
For example: 
 
whois <domain> 
 
dig <domain> 
 
nslookup <domain> 
 
whois google.com  
dig google.com  
  
nslookup google.com 

## 8.Vulnerability assessment: 
 a. Toperform Vulnerability assessment using nmap. 
 
 
Step1: 
 
Perform a vulnerability assessment using Nmap. You can use Nmap 
scripts for this: 
 
                     nmap --script vuln scanme.nmap.org 
 
## 9. Also perform the above tasks with other open source tools and 
compare the output. 
 
To compare the output, you can use other open-source tools like: 
• Masscan: For fast port scanning. 
• Zmap: Another fast port scanner. 
• OpenVAS: For vulnerability scanning. 
• Nikto: For web server scanning. 
 
 
sudo apt install masscan 

sudo masscan 172.217.167.46 -p443 
 
Zmap: Another fast port scanner 
  
 
• OpenVAS: For vulnerability scanning. 
 
 
OpenVAS and Nmap are both powerful tools used in the field of 
cybersecurity, particularly for vulnerability scanning and network mapping. 
However, they serve different primary purposes and have distinct features. 
Here's a comparison to help understand their roles: 
OpenVAS 
Primary Purpose: Vulnerability Scanning 
• Functionality: OpenVAS is designed to scan networks for known 
vulnerabilities. It identifies security issues by comparing the target 
system against a database of known vulnerabilities. 
• Features: 
• Extensive vulnerability database. 
• Detailed reporting on identified vulnerabilities. 
• Risk assessment and prioritization. 
• Integration with other security tools. 
• Use Case: Ideal for comprehensive vulnerability assessments and 
regular security audits. It helps organizations identify and mitigate 
potential security risks. 
 

## 10. Perform 5 more active scans using nmap and record what you had 
analyzed from it 
 
Perform five more active scans using Nmap and record your analysis. 
Here are some scan types you can try: 
 
1. SYN Scan: 
      nmap -sS 44.228.249.3 

 
2. FIN Scan: 
nmap -sF 44.228.249.3 
 
 
3. Xmas Scan: 
nmap -sX 44.228.249.3 
  
 
4. Null Scan: 
nmap -sN 44.228.249.3 
 
 
 
5. Ack Scan: 
nmap -sA 44.228.249.3
