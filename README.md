<h1>Performing-queries-on-Chronicle</h1>

<h2>Description</h2>
I'm are a security analyst at a financial services company. I receive an alert that an employee received a phishing email in their inbox. 
I review the alert and identify a suspicious domain name contained in the email's body: signin.office365x24.com. 
I need to determine whether any other employees have received phishing emails containing this domain and whether they have visited the domain. I will use Chronicle to investigate this domain.

<br />


<h2>Languages and Utilities Used</h2>

- <b>Chronicle</b> 

<h2>Lab walk-through:</h2>

<p align="center">
Task 1: Launch Chronicle
  <br>
<img src="https://i.gyazo.com/8fd3e8577e125baa058032424e0804c2.png" height="80%" width="80%" alt="tcpdump"/>
<br />
<br />
<p align="center">
Task 2: In the search bar, type signin.office365x24.com and click Search. Under DOMAINS, signin.office365x24.com will be listed. This tells you that the domain exists in the ingested data.
  <br>
  <img src="https://i.gyazo.com/b7974a4e958ae6637cbd8620b11fe596.png" height="80%" width="80%" alt="tcpdump"/>
  <br>
Task 3: Investigate the threat intelligence data 
<img src="https://i.gyazo.com/c2df01005c4cf458eb25c5725d693848.png" height="80%" width="80%" alt="tcpdump"/>
  <img src="https://i.gyazo.com/3d4331bdb3022c39aaa73e4bf3735a30.png" height="80%" width="80%" alt="tcpdump"/>
  <img src="https://i.gyazo.com/a4531164c00f96d02985a6fab86b38e1.png" height="80%" width="80%" alt="tcpdump"/>
  <img src="https://i.gyazo.com/0897c56e9ca7770724962846f7dc876c.png" height="80%" width="80%" alt="tcpdump"/>
  <br>
  <p align="center">
Task 4. Investigate the resolved IP address
  <br>
      <p align="center">
Investigate the IP address found under the RESOLVED IPS insight card to identify if the signin.office365x24.com domain uses another domain.
<br>
<p align="center">

* Under RESOLVED IPS, click the IP address 40.100.174.34.
* Evaluate the search results for this IP address and use your incident handler's journal to take note of the following:
* TIMELINE: Take note of the additional POST request. A new POST suggests that an asset may have been phished.
* ASSETS: Take note of the additional affected assets.
 <p align="center">
  
<p align="center">
<img src="https://i.gyazo.com/cbffb6c127c0309a44dd84eddc3f6c8f.png" height="80%" width="80%" alt="tcpdump"/>


