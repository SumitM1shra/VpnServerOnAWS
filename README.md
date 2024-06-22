# VpnServerOnAWS
This is a simple project of hosting own vpn server through AWS and connect our local machine to that server through vpn tunneling with no cost attached. I used openvpn as the access server to configure and install the vpn on our virtual server. 
![0](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/db15f6d1-ab5b-444b-9e08-58d886995933)
#Step-1: https://openvpn.net/as-docs/aws-ec2.html#strengthen-security-76631 this unveils step by step approach to access server for free on cloud service provider for free.
#Step-2: Setting up own cloud environment i.e.
![27](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/5f4c53a1-fc22-458d-805b-774ba8620298)
Name the EC2 instance and search for AMI's. Make sure the region is not the one that you're currently in i.e. change region to anyother.
![28](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/cb7568d5-3c27-4b0f-a542-b919aa8faf45)
Go to the search bar
![29](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/f0d4710e-2e7c-48fa-8aee-aa05322f9b79)
Type in access server in the search bar and select openvpn access server
![30](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/7613a11a-168a-4b84-8772-5cdcb1e57853)
Click on suscribe now or before launching our instances
![31](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/becd899e-ad94-4701-ac02-4db31de95a37)
Create new-key-pair or use an existinging one also select a t2.medium or t2.large for storage. Rest of the settings should be default and launch the instance.
#Step-3: Connect to the instance
![32](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/e123ce95-fa9a-48b9-9abb-2e5bb7698771)
Once the instance is running connect it with windows or SSH client.
Step-4: VM configuration
![3](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/661ff777-6a30-434f-9e53-f8773a3b3324)
![4](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/39f4155f-4540-4312-a8bc-cb65970880cc)
![5](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/aa8f3d27-5b49-4567-86f3-2609ac551cf8)
Follow the steps as per the instructions from the openvpn documentations guide. Once we enter the password and configuration is complete we will get admin and user url.
![6](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/af0793c7-294e-4b7b-9915-a7a73d83a09b)
![26](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/5602699a-96f9-4506-9885-b9ef14205a07)
Enter the username: openvpnas 
and password.
![7](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/7928c39f-4dd4-4555-ad88-5abc0e8571ad)
Press on Agree
![10](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/034719f5-ae71-4a14-a907-8247b3aa1cfb)
Something like this will pop up but as we can see there is no user connected.
![11](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/a3dd8581-6c53-4aa8-bdcf-96cf17aee665)
Open up user access url in another tab and enter the username and password. Select the respective UI that you're using
![12](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/8ae9dfac-15e6-4c37-a582-b1d6a49f18fe)
It will initiate a download
![13](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/427f525f-af97-4dfd-907e-ccc91a5bbaaa)
Once the download is complete open the app from downloads.
![16](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/527dca68-6452-421f-ab5c-002b675e16dd)
Wait till the installation is completed.
![17](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/51e06239-6df5-49ab-87d9-8fb97a647943)
Terms and conditions manual will openup, click on agree
![18](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/e1e5dbfe-1f93-4875-8bfd-db75d152578f)
Something like this will pop up try to toggle the button
![19](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/5de6ca24-c444-472d-a4f9-339b2f575e99)
Enter the password 
![20](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/5450e90e-4da6-4148-83cc-1199a2f53492)
Congratulations! VPN is connected. If not try checking the internet connection or respective cloud console if it's ruuning the ec2 instance or not.
![24](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/67ddb052-9d51-49a6-8135-6e9234993b73)
If we go back to own admin panel and check it should one user is connected. Maximum 2 users can be connected for free.
![21](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/b5b3a984-a3bc-4545-bff1-2b7ba98b8e39)
Go to your respective browser and check for your ip address
![23](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/48b9228f-70ea-4b1c-9380-7c60c3ec2758)
We can also verify the vpn connection by checking our internet speed and connectivity.
![25](https://github.com/SumitM1shra/VpnServerOnAWS/assets/126559101/01da007f-446d-4fd5-a2db-7d7f6bdba6e5)
Once the work is done disconnect the vpn and try again. Try to terminate the instance because it will start billing if used to longer time.

Special thanks to Piyush Garg for this amazing idea.
























