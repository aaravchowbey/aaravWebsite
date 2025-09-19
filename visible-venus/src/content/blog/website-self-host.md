---
title: 'How I host this website'
description: 'An explanation on why and how I am self-hosting this site.'
pubDate: 'Sept 09 2025'
heroImage: '../../assets/how-i-host.jpg'
---

An explanation of how and why I am self-hosting this site. This is not meant to be a tutorial. If you are attempting to replicate this, feel free to reach out to me and I can help however I can. 

## Why Self-Host?
I chose to self-host my website because I already had a home server. I've been self-hosting some applications since the start of 2025, so I had a pretty solid setup to work with. Something I didn't have any experience with was hosting something that was publicly accessible. I currently access my services by connecting to a VPN, but I can't have all potential users of my website do that. I really wanted to learn how to set that up. I also like the control of self-hosting. I have full control over pretty much everything. I can easily switch to a non-static website that makes API calls to retrieve content at any time. A lot of cloud providers don't make that process easy. I am also not expecting to have a lot of users on this site, so I don't really need the horsepower of a cloud provider. 

### Do I recommend self-hosting?
I don't recommend people self-host unless they already have the hardware for it or an interest in that side of the process. Developing a website and using a cloud provider is much easier, and you can avoid a lot of the struggles that self-hosting can cause. My website is not built to handle a lot of concurrent users, and if you expect to scale to a large audience then it's a lot of trouble to self-host for them as well. You also have to make sure that you are exposing your website in a secure manner. You don't want to leave unnecessary ports open, and I am not even sure if I am doing everything right. 

### How I am self-hosting
I am using Cloudflare as my domain registrar, an Oracle VPS for my public IP, and my home server to host my website static files. I have a WireGuard tunnel between my VPS and home server, and I use Nginx to direct traffic meant for the website. I am not going to go into specifics about setting up the hosting or my server setup. I do plan on making a post about my home server with some more details in the future. Feel free to reach out to me if this is something you want to try on your own. 

![User to Cloudflare to Oracle to Home Server to Ubuntu VM](../../assets/how-i-host-diagram.jpg "Diagram showing flow of traffic")

##### Why do I have a VPS?
My ISP uses CGNAT, which means that I don't get a public IP address. To get around this, I use a VPS (Virtual Private Server). Oracle has a free tier that doesn't have a time constraint associated with it. There are a few cloud providers that have free VPS options. I use Oracle because it's free as long as you provision your VPS within certain limits. I know AWS is another popular option, but their free tier only lasts a year. I know that using a VPS goes against the core principle of self-hosting, because I have to rely on a cloud provider. In my case, I keep all of my data on my home server, and only use the VPS for the public IP. I'll be making a detailed post on my home server setup in the future and cover the specifics of my setup. 



In this post, I’ll share why I chose to self-host my site and how I set it up. This isn’t a step-by-step guide, but feel free to reach out if you're exploring something similar.

## Why Self-Host?
My journey into self-hosting started because I already had a home server running various applications since early 2025. While I was comfortable with private services accessed via VPN, making something publicly accessible was new territory for me. I wanted to learn how to open up my site to the world, and self-hosting gave me the flexibility and control I was looking for.

With self-hosting, I can manage every aspect of my site, from the software stack to the hardware. If I ever want to switch from a static site to something dynamic, I can do so without restrictions from a cloud provider. Also, I’m not expecting heavy traffic, so I don’t need the resources or scalability that big cloud platforms offer.

### Should You Self-Host?
Self-hosting isn’t for everyone. If you already have the hardware and enjoy tinkering with servers and networking, it can be a rewarding experience. However, using a cloud provider is much simpler and avoids many of the headaches that come with managing your own infrastructure. My setup isn’t designed for lots of concurrent users, and scaling for a large audience would be challenging. Security is also a major concern, and you need to be diligent about how you configure your server.

### How I Self-Host
Here’s a quick overview of my setup:
- **Domain registration:** Cloudflare
- **Public IP address:** Oracle VPS (Virtual Private Server)
- **Website hosting:** Home server for static files
- **Secure connection:** WireGuard tunnel between VPS and home server
- **Traffic management:** Nginx

I won’t go into all the technical details here, but I plan to write more about my home server setup soon.

![User to Cloudflare to Oracle to Home Server to Ubuntu VM](../../assets/how-i-host-diagram.jpg "Diagram showing flow of traffic")

##### Why Use a VPS?
My internet provider uses CGNAT (Carrier-Grade NAT), which means I don’t get a public IP address at my apartment. To work around this, I use a VPS. I chose to go with Oracle’s free tier, which doesn’t expire as long as you stay within certain limits. Other providers like AWS offer free VPS options, but those are usually time-limited. While relying on a VPS isn’t pure self-hosting, I keep all my data on my home server and use the VPS only for its public IP.

I’ll share more details about my home server setup in a future post. If you have questions or want to try self-hosting yourself, feel free to reach out!