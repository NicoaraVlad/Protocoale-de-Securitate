# Protocoale-de-Securitate
There are many methods of performing this attack, this section will present some of the more common ones using Kali
Linux. The attack is possible if the attacker is connected to the same network as the potential victim. Target’s IP address and
gateway are needed in order to proceed with the attack. These can be found first using route -n for the gateway and nmap for
the rest of the IP addresses.

![1](https://user-images.githubusercontent.com/32314467/72373012-26e88b00-3710-11ea-9000-bc9611e273e6.jpeg)
![2](https://user-images.githubusercontent.com/32314467/72373013-26e88b00-3710-11ea-9d9f-12f6ec7bb4bb.jpeg)
Next, it is needed to reroute the traffic inbound to kali to the port that SSL Strip will be running on, which is by default 10000.

![3](https://user-images.githubusercontent.com/32314467/72373015-27812180-3710-11ea-94ce-91cbf1ed96f9.jpeg)
In order to do any MITM we need our box to act like a router and be able to forward packets that does not have its IP
address in it as the destination. This is done by activating IP forwarding.

![4](https://user-images.githubusercontent.com/32314467/72373017-27812180-3710-11ea-90a4-8485c5a7e823.jpeg)

Use the arpsoof utility to make the victim believe your machine is the gateway.

![5](https://user-images.githubusercontent.com/32314467/72373018-27812180-3710-11ea-80f7-43f7b2801ddc.jpeg)

Once the arpspoof is up and running a new terminal should be opened for the SSL Strip command.

![6](https://user-images.githubusercontent.com/32314467/72373020-2819b800-3710-11ea-94e6-db7fb036a0fc.jpeg)

This command listens on port 10000 and also writes the logs into a file.
For the last step, tracking the victim’s data in real time "watch" command is used to show the logs.

![7](https://user-images.githubusercontent.com/32314467/72373024-2819b800-3710-11ea-966c-9ece311da380.jpeg)

Other methods use advanced frameworks which help the attacker achieve a lot in short period of time.
WebSploit

![8](https://user-images.githubusercontent.com/32314467/72373025-2819b800-3710-11ea-86f7-09dce164e2ff.jpeg)

After entering the framework, man in the middle module can be selected from the various other modules. We can set the
options for the attack then.

![9](https://user-images.githubusercontent.com/32314467/72373026-2819b800-3710-11ea-9e32-d5dca80c1c08.jpeg)

We will need to set up the network interface, the Router IP and the Targeted IP.

![10](https://user-images.githubusercontent.com/32314467/72373027-2819b800-3710-11ea-9f0c-57533cea6d5c.jpeg)

The last thing to do is to select a sniffer from the list and then run the attack. The advantage of this framework is that it
provides an automated process, which makes things easier

![11](https://user-images.githubusercontent.com/32314467/72373028-28b24e80-3710-11ea-95b8-59f91a7957c3.jpeg)

MitMF

Man in the middle framework is another easy to use method. In the example shown below, an injection is made showing
the word "Hacked" on a random web page.

![12](https://user-images.githubusercontent.com/32314467/72373030-28b24e80-3710-11ea-9e87-3505c6638a0c.jpeg)
