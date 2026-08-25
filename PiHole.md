# Pi-Hole Project
1.	For the implementation I am using a Raspberry Pi 4 Model B 1 GB of RAM model with a 32 GB MicroSD card for storage of the OS
<!-- Image of Raspberry Pi here -->

2.	To begin I used Raspberry Pi Imager and use 64 bit Raspberry Pi OS to image MicroSD card within a bigger SD card connected to an SD card adaptor to my PC configuring the Pi with it’s hostname, admin profile, default SSID and PSK,  & Pi Connect.
<!-- Images of when imaging the card -->

3.	Once imaged, I took the MicroSD card out of the adaptors and placed it into the Pi to configure the boot up of the Pi

4.	Using PuTTY, I SSH’ed into the Raspberry Pi to perform Updates/Upgrade of the OS, reboot, and then installed Pi-Hole.  I took note of the websites it’ll be using, the IP address of the Pi, and the password to get into the admin page of Pi-Hole.
<!-- Images of the PiHole setup -->

5.	Researching around the internet for various blocklists (and whitelists) for ads, trackers, and malware prone sites, I decided on having a few custom lists specifically for malware and my LG WebOS tracker blocker along with 3 lists from the same list creator of varying degrees of strictness of their blocklists to have latitude of blocking and try out what works and doesn’t.  Once picked updated the Gravity Lists to load it into the Pi-Hole
<!-- Image of setting up block lists -->

6.	Testing on my PC & Mac Laptop by setting the default DNS IP address in IPv4 and IPv6 to point to the Pi-Hole.  Using adblock-tester.com and various other websites to check the degree it’s blocking the ads.  Additionally checked popular websites that could be used to make sure they aren’t blocking
<!-- Images of Before and After of the blocking -->

7.	Due to using Xfinity as the ISP and their router/modem, prevents IP reservations (important to keep the Pi-Hole in 1 address so not chasing the address around on individual devices), will not give access to change the DNS server it’s pointed to (set to Xfinity’s default servers address of 75.75.75.75 & 76.76.76.76, instead of to the Pi-Hole).  

    - Could potentially do a workaround setting the Pi-Hole as the DHCP server however the Xfinity router will still have a chance to serve as the DHCP server since can only limit what IP addresses it could serve and best to limit it is 1 address and could refresh it every 5 minutes to make sure it doesn’t have a hold of it

8.	Due to this limitation, full implementation hasn’t been put in place until maintenance with Xfinity is completed due to some interference & speed issues yet to be figured out though everything has worked up to implementation on the router side of things
   
9.	The ideal Plan A is get a stronger router that allows for customization to hook into the Xfinity router and set it to bridge mode to become a modem only and then implement the Pi-Hole without any of the Xfinity restrictions.
and could refresh it every 5 minutes to make sure it doesn’t have a hold of it
