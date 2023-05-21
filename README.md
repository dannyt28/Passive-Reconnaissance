<h1>Passive-Reconnaissance</h1>

<h2>Description</h2>
<p>
  Nmap is an invaluable utility employed by malicious actors to identify network hosts and the services associated with them. These adversaries employ this tool to unveil vulnerabilities present on targeted hosts and subsequently exploit them. This reconnaissance process will entail a manual and non-intrusive scan conducted on a Windows 10 Virtual Machine running within the VirtualBox environment, using the Google Chrome browser. The objective is to gather pertinent information about Uber, with the intention of utilizing it for the purpose of penetration testing.
</p>

<h2>Environments Used</h2>
<ul>
  <li>
    <p><b>Windows 10 VM</b></p>
  </li>
</ul>

<h2>IMPORTANT NOTE!</h2>
<p>For security reasons, IP addresses and other sensitive information in screenshots have been blurred out.</p>

<h2>Lab walk-through:</h2>

<h2>Screenshot 1:</h2>
<p align="center">
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

<h2>Screenshot 2:</h2>
<p align="center">
 Then, navigate to the "Company" section and proceed to select the "About Us" option.
</p>
<img src="https://i.imgur.com/ChD3cZr.png" height="80%" width="80%" alt="Disk Sanitization Steps" />


<h2>Screenshot 3:</h2>
<p align="center">
  Continue scrolling down the page until you locate the section titled "Company Info", and then proceed to click on the "See our leadership" link.
</p>
<img src="https://i.imgur.com/s4AhzFP.png" height="80%" width="80%" alt="Disk Sanitization Steps" />


<h2>Screenshot 4:</h2>
<p align="center">
  Upon clicking the "See our leadership" link, observe the presence of various Board Directors and members associated with Uber. Additionally, you have the option to select individual members to access their respective contact information. Further down the page, you will find additional details of similar nature.
</p>
<img src="https://i.imgur.com/00PLqmY.png" height="80%" width="80%" alt="Disk Sanitization Steps" />


<h2>Screenshot 5:</h2>
<p align="center">
  Using your web browser, access the website 'who.is'. Proceed to enter 'uber.com' into the designated search box, and then press the 'Enter' key to initiate the search.
</p>
<img src="https://i.imgur.com/DHwmAUi.png" height="80%" width="80%" alt="Disk Sanitization Steps" />
  
  
<h2>Screenshot 6:</h2>
<p align="center">
From the search results, make a note of the DNS servers obtained. Additionally, pay attention to any other significant information presented in the subsequent sections below.
</p>
<img src="https://i.imgur.com/0jEfZYE.png" height="80%" width="80%" alt="Disk Sanitization Steps" />

    
<h2>Screenshot 7:</h2>
<p align="center">
Within the same web browser, enter "dnsqueries.com" into the search bar and press the 'Enter' key.
</p>
<img src="https://i.imgur.com/mb2fHgY.png" height="80%" width="80%" alt="Disk Sanitization Steps" />

  
 <h2>Screenshot 8:</h2>
<p align="center">
Proceed to scroll down and locate the hostname box on the webpage. Within this box, enter the first DNS server obtained in step 2. Afterward, select the 'run tool' option to initiate the process.
</p>
<img src="https://i.imgur.com/AmcX3vF.png" height="80%" width="80%" alt="Disk Sanitization Steps" />


<h2>Screenshot 9:</h2>
<p align="center">

Take note of the IP address obtained from the results. Repeat the aforementioned steps (step 4) using the second DNS server provided.
</p>
<img src="https://i.imgur.com/pC336aa.png" height="80%" width="80%" alt="Disk Sanitization Steps" />

      
      
 <h2>Screenshot 10:</h2>
<p align="center">

Now, input "whois.arin.net" into the search bar above and press the 'Enter' key. Next, locate the upper right-hand corner and enter the first IP address obtained in the previous step. Press 'Enter' to initiate the search. Analyze the IP address range to confirm the association with the first two DNS servers. Additionally, observe that this information is linked to NSONE, a technology company presently collaborating with UBER.
</p>
<img src="https://i.imgur.com/WGNjoAC.png" height="80%" width="80%" alt="Disk Sanitization Steps" />

 <h2>Screenshot 11:</h2>
<p align="center">
Proceed to scroll down and examine the available point of contact information, carefully analyzing the obtained results.
</p>
<img src="https://i.imgur.com/0QutxLn.png" height="80%" width="80%" alt="Disk Sanitization Steps" />
  
 <h2>Screenshot 12:</h2>
<p align="center">
Enter the following URL 'elliot.org/company-contacts/uber/' into the search bar and press the 'Enter' key.
</p>
<img src="https://i.imgur.com/Khv38x7.png" height="80%" width="80%" alt="Disk Sanitization Steps" />
<ul>
  <li>
    <p>
      <b>Notice the Executive Contacts. Using these names and emails found, the data can be used as an attack vector.  </b>
    </p>
  </li>
</ul>  

