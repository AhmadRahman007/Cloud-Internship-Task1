# Internee.pk Cloud Deployment

This was my first task for the Internee.pk Cloud Internship — migrate and deploy the Internee.pk platform to a cloud-based infrastructure, with HTTPS enabled.

Going into this, I genuinely didn't know what a VM was or how any of this worked. This repo is basically the result of learning it hands-on over one sitting.

## What I actually did

- Spun up an **Ubuntu 22.04 VM on AWS EC2** (t3.micro, free tier)
- Installed and configured **Nginx** as the web server
- Pointed a free domain (`ahmedrehman.duckdns.org` via DuckDNS) to the server's public IP
- Got a real **SSL certificate via Let's Encrypt / Certbot**, so the site runs on HTTPS with a valid padlock, not just HTTP
- Set up **AWS budget alerts** first, before touching anything, so I wouldn't accidentally rack up charges
- Built a simple landing page for "Internee.pk" (since no site files were provided for this task) with sections for About, Programs, and Mentors, just to have something real running behind the server instead of the default Nginx page

## Live site

🔗 https://ahmedrehman.duckdns.org

## Stack

- AWS EC2 (Ubuntu 22.04)
- Nginx
- Let's Encrypt / Certbot
- DuckDNS (free dynamic DNS)
- Plain HTML/CSS for the landing page

## What I learned

Honestly, most of this was new to me — SSH, security groups, DNS, and how SSL certs actually get issued. The biggest realization was that "deploying to the cloud" isn't some big mysterious thing, it's just renting a Linux machine, installing normal server software on it, and telling the internet where to find it.

## Files in this repo

- `index.html` — the landing page served by Nginx
- `README.md` — this file
