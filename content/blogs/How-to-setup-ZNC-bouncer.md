---
title: "How to setup ZNC bouncer!"
date: 2020-08-10
type: "post"
---
After struggling for so many days today, finally, I could set up the ZNC bouncer. This blog post is about what steps I followed, the silly mistakes I made, and how I solved all of those. 

But before proceeding to all that, let's first see what ZNC bouncer is, what IRC is, and why everyone should try and use this awesome communication platform.

So let's get started -
IRC is a platform for real-time communication for open source contributors but not just limited to them; and anyone can use it. It works on a client-server networking protocol. Various organizations offer IRC servers, and users have to use a client program to log in to the IRC servers. There are different IRC clients that one can use. I started using Hexchat, it's beginner-friendly, and also, it's pretty easy to navigate in it. 

As I said above, the thing with IRC is that it's a platform for real-time communication, so you need to be connected to the server through your client program if you don't want to miss a message. But suppose in a channel you ask a question from someone, but when they saw the question and were answering, you are not connected to the IRC, so you didn't get to read the answer. To prevent this and to be able to keep connected with the IRC server all the time, we have a solution which is setiing up the bouncer, which would then store the messages for us when we are not connected to the server. One famous bouncer we have is [ZNC](https://wiki.znc.in/ZNC). To set up a bouncer, we need to have a server that we can use to host our bouncer, and then we can connect our IRC client with it.

I had the Github Student Pack, and with that, I got 50$ Digital Ocean credits. I used these to set up a droplet (a virtual private server). 

For setting up the server: 

1. Make an account on the Digital Ocean site; for this, you'd require to add your credit card details, and an amount of around 10$ will be deducted from your account but then will be reverted in just a few minutes. This is to check the validity of the card. After this, you can access your account.

2. For availing of the free credits using Github Student Pack, go to your account and get a promo code for Digital Ocean. Then enter that promo code in the billing section on your Digital Ocean account, and now you will have the credits and can easily avail yourself those. 

3. Because I just needed a server to host a bouncer, I chose a 5$/month plan. One can select any plan as per their need if they plan to use it for other services. In the data center, choose the one closest to you to have the least latency.

4. Now that you have your credits, you can go on and create a droplet. For authentication, you can either go for a Password or can use an SSH key.

    For creating an SSH key go on to your terminal and use the following command:

    ``ssh-keygen`` This would generate a new SSH key.

    ``cat ~/.ssh/id_rsa.pub`` This would give you your public key, which you can add there.

    And after all, this, hit the create option, and your server will be up and running.



5. Now, you can open your terminal and access the server you have set up. For this, run the following command in the terminal:

    ``ssh root@<droplet_ip>`` 
    (if you used ssh) and hit enter.

    ``root@<droplet_ip>`` 
    (if you used a password) enter the password and hit enter.

    Now you have access to the server.

6. Now, we will go on to install and configure the ZNC bouncer. I followed this [tutorial](https://www.digitalocean.com/community/tutorials/how-to-install-znc-an-irc-bouncer-on-an-ubuntu-vps). It is pretty easy to follow and clearly explains all the steps. There are a few comments at the end of the post which are also good, and you might want to read them.

    After doing all that is mentioned in the blog above, you'd be able to access the web interface for the ZNC; you can then log in with the credentials you provided while configuring and adding/deleting users, networks, or changing various settings. 

7. You can now add this to whatever client program you are using. If you use Hexchat, add a new network and edit it. Add this **<droplet_id>/port** and all the other settings in the network. If you are using IRC for the first time, you should register your nick on IRC. Refer this [blog](https://freenode.net/kb/answer/registration) for that. 

It's quite fun to use IRC, from setting it up and exploring it for the first time to learning from awesome folks you will find there on various channels. 
If you face any issues in setting up, feel free to reach out to me through email, I'll be happy to help. :)

So, that was quite fun and satisfying to host my ZNC bouncer finally. I made some silly mistakes, like I was setting and installing the ZNC onto my machine without accessing the server as root and wondering why I couldn't access the web interface. Ensure to note all the passwords or use a password manager to store all passwords you are using while configuring the bouncer to avoid re-setting passwords. 

Finally, it's time when I can close all of the tabs that I opened for searching different things related to setting up the bouncer. 
If you want to avoid doing all this but want a ZNC account, I will be more than happy to add you to my bouncer. Let me know through email. :)