---
layout: post
title: "How to setup ZNC bouncer!"
date: 2020-9-10
---
After struggling for so many days today finally I could set up the ZNC bouncer. This blog post is about what steps I followed, silly mistakes I did, and also then how I solved all those. 

But before proceeding to all that, let's first see what is ZNC bouncer, what is IRC, and also why everyone should try and use this awesome communication platform.

So let's get started -
IRC is a platform for real-time communication for open source contributors but not just limited to them and anyone can use it. It works on a client-server networking protocol. There are various organisations which offer IRC servers and for users they have to use a client program, using which they will then login to the IRC servers. There are various IRC clients which one can use. I started using Hexchat, it's beginner friendly and also it's quite easy to navigate in it. 

Now the thing with IRC as I said above is that it's a platform for real-time communication, so you need to be connected to the server through your client program all the time if you don't want to miss a message. But suppose in a channel (In IRC we have various public channels and in those channels we have folks who join those channels and communicate witt each other) you ask a question to someone but when they saw the question and were answering you were not connected to the IRC, so you didn't get to read the answer. To prevent this and to be able to keep connected with IRC server all the time we have a solution which is setiing up the bouncer, which would then store the messages for us, when we are not connected to the server. One of the popular bouncer we have is [ZNC](https://wiki.znc.in/ZNC). To set up a bouncer we need to have a server which we can use to host our bouncer on and then we can connect our IRC client with it.

I had the Github Student Pack and with that I got 50$ Digital Ocean credits. I used these to setup a droplet (it's a virtual private server). 

For setting up the server: 

1. Make an account on the Digital Ocean site, for this you'd require to add your credit card details and an amount of around 10$ will be deducted from your account but then will be reverted back in just a few minutes. This is just to check the valadity of the card. After this you can access your account.

2. For availing the free credits using Github Student Pack, go to your account and get a promo code for Digital Ocean. Then enter that promo code in the billing section on your Digital Ocean account and now you will have the credits and can easily avail those. 

3. Because I just needed a server for hosting a bouncer, I chose 5$/month plan. One can choose any plan as per their need in case they are planning to use it for other services too. In the data centre choose the one closest to you to so that you have least latency.

4. Now that you have your credits, you can go on and create a droplet. For authentication you can either go for a Password or can use SSH key.

For creating ssh key go on to your terminal and use the follwing command:

`ssh-keygen`  -This would generate a new SSH key.

`cat ~/.ssh/id_rsa.pub` -This would give you your public key which you can add there.

And after all this hit the create option and your server will be up and running.



5. After this open your terminal and access the server you have set up. For this run the following command in the terminal:

`ssh root@<droplet_ip>` (if you used ssh) and hit enter.
`root@<droplet_ip>` (if you used a password) enter the password and hit enter.

Now you have the access to the server.

6. Now we will go on to install and configure the ZNC bouncer. I followed this [tutorial](https://www.digitalocean.com/community/tutorials/how-to-install-znc-an-irc-bouncer-on-an-ubuntu-vps). It is pretty easy to follow and clearly explains all the steps. There are a few comments at the end of the post which are also good and you might want to read.

After doing all that is mentioned in the blog above you'd be able to access the web interface for the ZNC, and from there you can then login with the credentials you provided while configuring and can add/delete users, networks or change various settings. 

7. You can now add this in whatever client program you are using. If you are using Hexchat then add a new network and edit it. Add in the network add this **<droplet_id>/port** and all the other settings too. In case you are using IRC for the first time, you should register your nick on IRC. Refer this [blog](https://freenode.net/kb/answer/registration) for that. 

It's quit fun to use IRC right from setting it up and exploring it for the fisrt time and then to learning from awesome folks you will find there on various channels. 
If you face any issues in setting up feel free to reach out me through email I'll be happy to help. :)

So, that was quite fun and satisfying, to finally host my own ZNC bouncer. I did some silly mistakes like I was setting and installing the ZNC on to my machine without accessing the server as root and wondering why I can't access the web interface. Make sure to note all the passwords or use a password manager to store all passwords you are using while configuring the bouncer to avoid nuisance of re-setting passwords. 

Finally it's time when I can close all of the tabs that I opened for searching different things related to setting up the bouncer. 
If you want to avoid doing all this but want a ZNC account, I will be more than happy to add you on my bouncer. Let me know through email. :)