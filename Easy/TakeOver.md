Link: https://tryhackme.com/room/takeover


<img width="512" height="512" alt="image" src="https://github.com/user-attachments/assets/5d3d1b7f-ba7b-49e0-afdc-41b458f8b454" />

This challenge revolves around subdomain enumeration.

**Task 1: Help Us**

Hello there,

I am the CEO and one of the co-founders of futurevera.thm. In Futurevera, we believe that the future is in space. We do a lot of space research and write blogs about it. We used to help students with space questions, but we are rebuilding our support.

Recently blackhat hackers approached us saying they could takeover and are asking us for a big ransom. Please help us to find what they can takeover.

Our website is located at https://futurevera.thm

Hint: Don't forget to add the 10.201.17.174 in /etc/hosts for futurevera.thm ; )

**Answer the questions below**

Q1. _What's the value of the flag?_

Answer: `flag{beea0d6edfcee06a59b83fb50ae81b2f}`

**_Explanation:_**

1. We first add our MACHINE_IP to /etc/hosts 

<img width="731" height="304" alt="image" src="https://github.com/user-attachments/assets/2f03c243-10b0-4d15-85f3-c6b05417ba06" />

2. We try to get the response size for non-existent subdomains 

`curl -sk https://10.201.17.174 -H "Host: doesnotexist.futurevera.thm" | wc -c`

<img width="1000" height="113" alt="image" src="https://github.com/user-attachments/assets/b39e1f65-9dc0-442b-b49a-5b3ba657c059" />


3. We use fluff to get the subdomains for futurevera.thm using the following command

`ffuf -w /usr/share/wordlists/seclists/Discovery/DNS/namelist.txt \ 
     -H "Host: FUZZ.futurevera.thm" \
     -u https://10.201.17.174 \
     -fs 4605 \
     -k`

We find two sub-domains when we run the above command

<img width="1246" height="803" alt="image" src="https://github.com/user-attachments/assets/e6666156-894e-4660-a362-a3b28593dc1e" />

4. Now we try to visit both of the sub-domains

https://blog.futurevera.thm/

<img width="1919" height="1001" alt="image" src="https://github.com/user-attachments/assets/7c82efaf-1fcd-4cf9-ab6c-b09ac6f1a6f8" />

We don't find much on this 

<img width="1920" height="1000" alt="image" src="https://github.com/user-attachments/assets/cdee2181-8471-47ad-b6e2-eb2d2ea2aebd" />

Now we move on to https://support.futurevera.thm/

<img width="1917" height="1001" alt="image" src="https://github.com/user-attachments/assets/155d9f61-7f8f-4ea6-b494-9b9420e06ad8" />

5. We click on Advanced and View Certificate

<img width="978" height="652" alt="image" src="https://github.com/user-attachments/assets/f658243c-0992-4bc4-a890-473973ab8132" />

6. In the Certificate we can see Subject Alt Names and we try to open it

<img width="801" height="117" alt="image" src="https://github.com/user-attachments/assets/a670f1e0-0feb-453b-a8d1-80d9a529e375" />

7. We can see the flag now

<img width="1920" height="983" alt="image" src="https://github.com/user-attachments/assets/d0b07cc2-c015-4056-a5e6-316e568e50aa" />

---
