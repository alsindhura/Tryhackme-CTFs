Link: https://tryhackme.com/room/lofi

We spawn the VM and visit the website

<img width="1182" height="644" alt="image" src="https://github.com/user-attachments/assets/36ba8a02-fce4-400a-b3b2-daa8d43e7ef0" />

We see the CTF challenge hinting about two rooms and both have content about `Path Traversal`

When we click any of the items listed under Discography, we can see something like this `http://MACHINE_IP/?page=relax.php`

So we try to access sensitive files using this `?page=` 

Initially, we try this payload `http://MACHINE_IP/?page=/etc/passwd` and we are shown a banner like below

<img width="750" height="223" alt="image" src="https://github.com/user-attachments/assets/232f2bed-cbe4-4d65-a915-e18f1a9979bb" />

Now we try to move up to the root (`/`) and our new URL would be `http://MACHINE_IP/?page=../../../etc/passwd`

And we can see the content of /etc/passwd which shows that this application is vulnerable to LFI

<img width="759" height="361" alt="image" src="https://github.com/user-attachments/assets/129ad775-9004-48b8-823f-754b36cba1f3" />

We need to access the flag in the `/` directory and our URL becomes `http://MACHINE_IP/?page=../../../flag.txt` and finally we can see the flag

<img width="768" height="232" alt="image" src="https://github.com/user-attachments/assets/255a98e2-2762-4d98-bf2b-0dbdbb2f00c8" />

Flag: `flag{e4478e0eab69bd642b8238765dcb7d18}`

__________________________________________________
