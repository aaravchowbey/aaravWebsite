---
title: 'How I host this website'
description: 'An explanation on why and how I am self-hosting this site.'
pubDate: 'Sept 09 2025'
heroImage: '../../assets/how-i-host.jpg'
---

An explanation on how and why I am self-hosting this site. 

## Why Self-host

- talk about why im self hosting
    - i have a server
    - i wanted to learn how it works
    - I like the control of it
    - i am not expecting a lot of users

### Do I reccomend self-hosting
    - no, its not necessary and the cloud options are so much easier
    - only do it if its something youre interested in
    - website isnt built to handle a lot of users, but if you need that use cloud
    - security risks

## How I am self hosting
    - diagram showing flow
    - briefly talk about why I am using oracle vps, talk about how a future post will come out about a detailed explanation on setting up server
    - talk about ci/cd workflow
        - polling
        - if i had a public ip i would use webhooks
        - dev branch
    - Cloudflare


## Why Self-Host?
I chose to self-host my website because I already had a home server. I've been self-hosting some applications since the start of 2025, so I had a pretty solid setup to work with. Something that I didn't have any experience with was hosting something that was publicly accessible. I currently access my services by connecting to a vpn, but I can't have all potential user's of my website do that. I really wanted to learn how to set that up. I also like the control of self-hosting. I have full control over pretty much everything. I can easily switch to a non-static website that makes API calls to retrive content at any time. A lot of cloud providers don't make that process easy. I am also not expecting to have a lot of users on this site, so I don't really need the horsepower of a cloud provider. 

### Do I recommend self-hosting
I don't recommend people self-host unless they already have the hardware for it or an interest in that side of the process. Developing a website and using a cloud provider is much easier, and you can avoid a lot of the struggles that self-hosting can cause. My website is not built to handle a lot of concurrent users, and if you expect to scale to a large audience then it's a lot of trouble to self-host for them as wlel. You also have to make sure that you are exposing your website in a secure manner. You don't want to leave unneccesary ports open, and I am not even sure if I am doing everything right. 

### How I am self-hosting
I am using cloudflare for my domain name, an Oracle VPS for my public IP, and my home server to host my website static files. I have a wireguard tunnel between my VPS and home server, and I use nginx to direct traffic meant for the website. 

##### Why do I have a VPS?
My ISP uses CGNAT, which means that I don't get a public IP address. To get around this, I use a VPS (Virtual Private Server). Oracle has a free tier that doesn't have a time constraint associated with it. There are a few cloud providers that have free VPS options. I use Oracle because it's free as long as you provision your VPS within certain limits. I know AWS is another popular option, but their free tier only lasts a year. I know that using a VPS goes against the core principle of self-hosting, because I have to rely on a cloud provider. In my case, I keep all of my data on my home server, and only use the VPS for the public IP. I'll be making a detailed post on my home server setup in the future and cover the specifics on my setup. 


