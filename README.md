# Passive-Reconnaissance

<h2>Description</h2>
Nmap is an invaluable utility employed by malicious actors to identify network hosts and the services associated with them. These adversaries employ this tool to unveil vulnerabilities present on targeted hosts and subsequently exploit them. This reconnaissance process will entail a manual and non-intrusive scan conducted on a Windows 10 Virtual Machine running within the VirtualBox environment, using the Google Chrome browser. The objective is to gather pertinent information about Uber, with the intention of utilizing it for the purpose of penetration testing.
<br />



<h2>Environments Used </h2>

- <b>Windows 10 VM </b> 

<h2>IMPORTANT NOTE!</h2>
For security reasons, IP addresses and other sensitive information in screenshots have been blurred out. 

<h2>Lab walk-through:</h2>

<h2>Screenshot 1:</h2>
<p align="center">
Step 1: <br/>
Launch your web browser and direct it to Uber's official company homepage, accessible at Uber.com.
</p>
<img src="https://i.imgur.com/yo8UzxQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<ul>
  <li>
    <p>
      <b>Locate the designated user interface element positioned at the upper right-hand corner of the webpage, which consists of two horizontal lines.</b>
    </p>
  </li>
</ul>
<ul>
  <li>
    <p>
      <b>Execute a click action on the aforementioned user interface element to activate its associated functionality.</b>
    </p>
  </li>
</ul>

<h2>Screenshot 2:</h2>
<p align="center">
Step 2: <br/>
Then, navigate to the "Company" section and proceed to select the "About Us" option.
</p>
<img src="https://i.imgur.com/ChD3cZr.png" height="80%" width="80%" alt="Disk Sanitization Steps" />
<ul>
  <li>
    <p>

<h2>Screenshot 3:</h2>
<p align="center">
Step 3: <br/>
Continue scrolling down the page until you locate the section titled "Company Info", and then proceed to click on the "See our leadership" link.
</p>
<img src="https://i.imgur.com/s4AhzFP.png" height="80%" width="80%" alt="Disk Sanitization Steps" />
<ul>
  <li>
    <p>
   
  
<h2>Screenshot 4:</h2>
<p align="center"> <br/>
Extended Output from above 
</p>
<img src="https://i.imgur.com/ANfVmP5.png" height="80%" width="80%" alt="Disk Sanitization Steps" />
<ul>
  <li>
    <p>
      <b>Multiple svchost.exe processes occurring concurrently with different process IDs, such as 1220, 1004, and others, raise concerns regarding the identification of the legitimate svchost.exe process. This situation highlights a potential threat, as determining the correct svchost.exe process becomes crucial for distinguishing normal system behavior from malicious activity.</b>
    </p>
  </li>
  <li>
    <p>
      <b>Additionally, the reader_sl.exe process triggers suspicion based on its associated process ID (PID). Further investigation is warranted to determine the nature of this process and evaluate its potential impact on system security.Identifying and understanding the true nature of svchost.exe processes and scrutinizing the reader_sl.exe process will contribute to a more comprehensive assessment of system integrity and aid in mitigating potential security risks.</b>
    </p>
  </li>
</ul>
 
<h2>Screenshot 5:</h2>
<p align="center">
Pslist plugin command: "vol.py -f cridex.vmem pslist" <br/>
</p>
<img src="https://i.imgur.com/l67RQHr.png" height="80%" width="80%" alt="Disk Sanitization Steps" />
<ul>
  <li>
    <p>
      <b>Analysis: The examination of the memory image has uncovered multiple suspicious processes, raising concerns about the system's integrity and security. One notable finding is the 'Reader_sl.exe' process with a PID of 1640, which exhibits a relationship with 'explorer.exe' processes (PPID: 1484). This association demands further investigation to assess potential unauthorized interactions or suspicious activities. </b>
    </p>
  </li>
  <li>
    <p>
      <b>Additionally, the 'Alg.exe' process with a process ID has a 'svchost.exe' process parent ID (PPID) of 652. This relationship raises questions about the purpose and legitimacy of the 'Alg.exe' process, prompting further investigation to assess its impact on system security.Furthermore, the 'wuauclt.exe' process is observed with two different process IDs, indicating potential inconsistencies or duplication. Understanding the reasons behind this discrepancy is crucial to determine if it signifies malicious activity or system misconfiguration.</b>
    </p>
  </li>
  <li>
    <p>
      <b>Thorough analysis and scrutiny of these suspicious processes will contribute to a comprehensive assessment of the system's security posture, allowing for effective mitigation of potential risks and ensuring the integrity of the forensic investigation.</b>
    </p>
  </li>
</ul>
  
  
<h2>Screenshot 6:</h2>
<p align="center">
Network Connections command: “vol.py -f cridex.vmem connections” <br/>
</p>
<img src="https://i.imgur.com/0Kn0SVF.png" height="80%" width="80%" alt="Disk Sanitization Steps" />
<ul>
  <li>
    <p>
      <b>Analysis: Examination of network connections within the memory image provided insights into the connectivity patterns between local and remote addresses. The local address which was private, signifies that the connection originated from within a local network environment.</b>
    </p>
  </li>
  <li>
    <p>
      <b>The remote address was located in South Africa and was associated with a specific house as well. Website 'ipgeolocation.io' was used to shed light on the potential location of the remote entity involved in the connection. </b>
    </p>
  </li>
  <li>
    <p>
      <b>The presence of a network connection between a private local address and a remote address in South Africa, suggests communication between systems within the local network and an external entity located in that region. Further investigation is necessary to ascertain the nature and purpose of the connection. 
    </p>
  </li>
</ul>
  
  
  
  
<h2>Conclusion</h2>
Performing live system forensics requires precision to avoid losing crucial evidence. In this project, industry-standard forensic recovery tools were utilized to conduct a live system memory analysis. The investigation involved capturing a live image of the host system's RAM using AccessData FTK Imager on a Windows 10 VM and analyzing the captured memory image using Volatility on a SIFT VM. The focus of the investigation encompassed the examination of operating system processes, registries, log files, and hashes. Detailed methodology and findings were meticulously documented in a comprehensive Microsoft Word report, including step-by-step screen captures. The report serves as complete forensic lab notes, establishing the investigator's expertise as a potential witness in court proceedings, if required.
