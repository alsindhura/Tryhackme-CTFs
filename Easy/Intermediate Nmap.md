Link: https://tryhackme.com/room/intermediatenmap (Premium Room)

First we spawn the VM

Now we find all the open ports using the command `nmap -p- MACHINE_IP`

<img width="1016" height="372" alt="image" src="https://github.com/user-attachments/assets/84d4a647-6d51-4d30-bb23-f1a815818744" />

We see a port `31337`. I open `http://MACHINE_IP:31337` and see credentials

<img width="251" height="64" alt="image" src="https://github.com/user-attachments/assets/d1d26c94-3357-40fc-a8ab-2fb824bcd0f6" />

From our Nmap output, we saw that SSH was running on port 22, so we attempted to log in via SSH

<img width="971" height="197" alt="image" src="https://github.com/user-attachments/assets/6fc8f011-2f06-40ad-a7f2-02110001c3b7" />

We enter the password which we got earlier (i.e `Dafdas!!/str0ng`)

We have logged in

<img width="1026" height="785" alt="image" src="https://github.com/user-attachments/assets/66646df2-0a82-4cfa-a25b-9fca8a167107" />

We try to list the files and folders using `ls -la` but we found no flag 

<img width="716" height="266" alt="image" src="https://github.com/user-attachments/assets/46b54b91-ea90-4982-a76d-69b1c64ec3b8" />

I will try to move one directory up using cd .. and here I find a folder named `user`

<img width="632" height="182" alt="image" src="https://github.com/user-attachments/assets/c1069686-780c-4932-8f72-cbec824b47ba" />

Let's see what is inside this folder

<img width="609" height="154" alt="image" src="https://github.com/user-attachments/assets/7528456d-3999-4d2e-9d81-d420dd17ca80" />

We can see the flag 

<img width="690" height="73" alt="image" src="https://github.com/user-attachments/assets/b625a98d-13f0-4418-93e9-c44c7c34bf12" />

Flag: `flag{251f309497a18888dde5222761ea88e4}`

____________________________________________________


