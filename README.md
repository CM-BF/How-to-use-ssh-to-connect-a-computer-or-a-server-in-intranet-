# How-to-use-ssh-to-connect-a-computer-or-a-server-in-intranet

 **Have you met this problem that when you wanna use ssh to connect to your new server and begin your work at home but immediately you realized that your server doesn't have a public ip address?**

#### There are three solutions which may help you.

## 1. Using a VPN connection

If you can ask for a VPN account from your boss and your company indeed has installed VPN, just ask for it.

## 2. Using a Reverse SSH connection

It's true that you cannot ssh connect from a public ip computer to a private ip computer directly, but there is a way-round.

You can resort to google for a bunch of tutorials. There are two general methods:

* With a VPS, you can map the ssh service from your intranet server(A) to a port of your VPS server(B). Then you can always connect to it using A_user@B_address -p B_mapping_port.
* Without a VPS, you can only map the ssh service from your intranet server(A) to your own computer. Then use A_user@localhost -p your_port to connect. The flaws are that it cannot work if your computer doesn't have a public ip and it is troublesome if your public ip is dynamic (you have to reopen the reverse service every time you change your ip).

## 3. Using IPv6 to connect

Fortunately, if you can access IPv6 network and your intranet server also has an public IPv6 ip, you can using IPv6 to connect.



### All the methods above only point out the directions. There are so many tutorials on the internet, so I guess it is easy for your guys to find it.