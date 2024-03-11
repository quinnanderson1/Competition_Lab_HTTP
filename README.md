<h1>Creating an HTTP Server</h1>

<h2>Description</h2>
This portion of the project is to configure an Apache2 web server in Ubuntu. 
<br />

<h2>Install Apache2</h2>

The systems hadn’t been updated or upgraded since installing them, so the Ubuntu system didn’t have the Apache2 package in its repositories. After updating the system, Apache2 was installed and started running right away with the default webpage and configuration. 

<h2>Allow Apache through UFW</h2>

To ensure the system’s firewall would have the right rules to allow for web traffic if it was ever enabled, the Apache profile was enabled through UFW. The firewall was not enabled for the sake of simplicity. This step was new to me, as I hadn’t worked with the UFW before. 

<h2>Check Default Webpage from Internal Machines</h2>

Now that the Apache service is up and running, the internal machines should be able to access the default webpage. The Ubuntu and Kali machines pulled up the webpage in Firefox without any problems, and the CentOS machine curled the default page without a hitch.

<h2>Forward Port 80 through CentOS</h2>

Now that all the internal machines can access the webpage, it’s time to configure the CentOS machine to forward traffic on port 80 to the Ubuntu web server. The rule was added to the external zone so that any machine on the home network can access the Ubuntu web server by typing in the IP address of the external CentOS interface. 

<h2>Test Default Webpage through External Systems</h2>

The last step to ensure this project worked is to check for connectivity from the machines connected to the home network. Thankfully, this project yielded no issues, and everything worked with the initial configuration. 

<h2>Screenshots:</h2>

<p align="center">
Update Machines: <br/>
<img src="https://i.imgur.com/22FpTXp.png" height="60%" width="60%" alt="Update Machines"/>
<br />
<br />
Install Apache2: <br/>
<img src="https://i.imgur.com/Vi3OFyk.png" height="60%" width="60%" alt="Install Apache2"/>
<br />
<br />
Apache2 is Running: <br/>
<img src="https://i.imgur.com/PgVN809.png" height="60%" width="60%" alt="Apache2 is Running"/>
<br />
<br />
Change UFW Rules: <br/>
<img src="https://i.imgur.com/yyZ5Qra.png" height="60%" width="60%" alt="Change UFW Rules"/>
<br />
<br />
Default Webpage on Internal Machines: <br/>
<img src="https://i.imgur.com/jsR3rxN.png" height="60%" width="60%" alt="Default Webpage on Internal Machines"/>
<br />
<br />
Forward Port 80: <br/>
<img src="https://i.imgur.com/Ff185Fr.png" height="60%" width="60%" alt="Forward Port 80"/>
<br />
<br />
External Machine Check #1: <br/>
<img src="https://i.imgur.com/fFz5Tno.png" height="60%" width="60%" alt="External Machine Check #1"/>
<br />
<br />
External Machine Check #2: <br/>
<img src="https://i.imgur.com/droyqHh.jpeg" height="60%" width="60%" alt="External Machine Check #2"/>
<br />

</p>
