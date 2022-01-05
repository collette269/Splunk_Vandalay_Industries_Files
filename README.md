# Splunk_Vandalay_Industries_Files

Unit 18 Homework: Lets go Splunking!

Rice University, Boot Camp Certificate Program, Cyber Security

Data provided by Trilogy Education Services, a 2U, Inc. brand.

Scenario
You have just been hired as an SOC Analyst by Vandalay Industries, an importing and exporting company.
Vandalay Industries uses Splunk for their security monitoring and have been experiencing a variety of security issues against their online systems over the past few months.
You are tasked with developing searches, custom reports and alerts to monitor Vandalay's security environment in order to protect them from future attacks.

Background 
As the worldwide leader of importing and exporting, Vandalay Industries has been the target of many adversaries attempting to disrupt their online business. Recently, Vandaly has been experiencing DDOS attacks against their web servers.Not only were web servers taken offline by a DDOS attack, but upload and download speed were also significantly impacted after the outage. Your networking team provided results of a network speed run around the time of the latest DDOS attack.

STEP 1: Analyze Data using https://www.splunk.com/

![image](https://user-images.githubusercontent.com/88781846/148220690-6042a4e9-3808-4a93-b1c1-12bc9eeab7ef.png)

![image](https://user-images.githubusercontent.com/88781846/148220725-45bcc22a-de8d-481a-9109-99f3a1a92de0.png)

![image](https://user-images.githubusercontent.com/88781846/148221244-0a7b84ef-44c9-41d6-9767-c189f5e3e441.png)

![image](https://user-images.githubusercontent.com/88781846/148221263-1adcd61a-70e8-4793-becb-555f27828eb0.png)

![image](https://user-images.githubusercontent.com/88781846/148221318-1af95077-6583-4d80-8b9d-9a6804f8c99c.png)

![image](https://user-images.githubusercontent.com/88781846/148221399-3d6051de-ec8d-44e3-9bca-00faa4e05a84.png)

![image](https://user-images.githubusercontent.com/88781846/148221458-cd05e078-f56b-486e-9e80-b47f20b55b1a.png)

![image](https://user-images.githubusercontent.com/88781846/148221480-b777bac4-3684-4d17-8679-cd1451565797.png)

![image](https://user-images.githubusercontent.com/88781846/148221519-0611c9df-d2a3-43ee-bbb5-634c3e29f35c.png)

![image](https://user-images.githubusercontent.com/88781846/148221570-15c07231-7402-4368-9b43-f160e58c5018.png)

Analysis
Distributed denial of service (DDoS) attack occurs from multiple connected online devices including the use of botnets in an effort to overwhelm website traffic. Vandalay Industries servers wser taken offline from 2.23.2020 midnight -2.24.2020 midnight (24 hours) and the download and upload speeds were affected. 

STEP 2: Identify Critical Vulnerabilities

Background
Due to the frequency of attacks, your manager needs to be sure that sensitive customer data on their servers is not vulnerable. Since Vandalay uses Nessus vulnerability scanners, you have pulled the last 24 hours of scans to see if there are any critical vulnerabilities.

For more information on Nessus, read the following link: https://www.tenable.com/products/nessus

![image](https://user-images.githubusercontent.com/88781846/148221944-a47ec434-b95e-46ad-92d7-42bd57b4812a.png)

![image](https://user-images.githubusercontent.com/88781846/148221970-d0b95372-dc04-46d5-9f1a-3615f8e4626b.png)

![image](https://user-images.githubusercontent.com/88781846/148221998-ce1aea53-73a9-4458-9208-f498da7560f9.png)

![image](https://user-images.githubusercontent.com/88781846/148222046-8591d0dc-68c3-415d-b2a0-7f8ebdebc382.png)

![image](https://user-images.githubusercontent.com/88781846/148222067-2a7caf42-1f88-4702-bf82-f6178588debe.png)

Analysis 
In the past 24 hours, Nessus has identified 243 events on website server IP address 10.11.36.23 with 368 counts (19.9%) of events with "critical" severity. To identify this issue in the future, the Alert “Count of Critical Vulnerabilities” has been created to email <soc@vandalay.com> the quantity of "critical" events at midnight for the previous 24 hours. 

Step 3: Drawing the baseline

Background
A Vandaly server is also experiencing brute force attacks into their administrator account. Management would like you to set up monitoring to notify the SOC team if a brute force attack occurs again.

![image](https://user-images.githubusercontent.com/88781846/148223459-e6b20b2e-dfc9-42e8-8e07-04b671136b85.png)

![image](https://user-images.githubusercontent.com/88781846/148223501-b9d27e39-1e3e-451a-9e0f-f5fc2d37a6a3.png)

![image](https://user-images.githubusercontent.com/88781846/148223522-2e35a6a2-92bc-46f8-a832-028379f028d5.png)

![image](https://user-images.githubusercontent.com/88781846/148223537-a8c279a1-2744-4bb2-9b4d-4ee041b39afa.png)

Analysis
After reviewing the Administrative Logs, the estimated baseline for failed login attempts is 30 times an hour. During the brute force attack, the failed logins was anywhere from 50-70 times an hour. To identify further attacks, an Alert was created titled "Brute Force Attack" and would be emailed to <SOC@vandalay.com> if the failed login count exceeded 30 times during an hour time interval. 




