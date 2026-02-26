Link: https://tryhackme.com/room/corridor

Start the machine and go to `http://MACHINE_IP`

<img width="1920" height="957" alt="image" src="https://github.com/user-attachments/assets/38f8f68f-7517-4cff-b768-b200baeaa4a2" />

We can see a corridor with doors and note that these door navigate to a new page.

Let's click on the first door and we see the link as `http://MACHINE_IP/c4ca4238a0b923820dcc509a6f75849b`

And refer the table below for all 13 doors

| door   | link |
|--------|------|
| door1  | http://MACHINE_IP/c4ca4238a0b923820dcc509a6f75849b |
| door2  | http://MACHINE_IP/c81e728d9d4c2f636f067f89cc14862c |
| door3  | http://MACHINE_IP/eccbc87e4b5ce2fe28308fd9f2a7baf3 |
| door4  | http://MACHINE_IP/a87ff679a2f3e71d9181a67b7542122c |
| door5  | http://MACHINE_IP/e4da3b7fbbce2345d7772b0674a318d5 |
| door6  | http://MACHINE_IP/1679091c5a880faf6fb5e6087eb1b2dc |
| door7  | http://MACHINE_IP/c9f0f895fb98ab9159f51fd0297e236d |
| door8  | http://MACHINE_IP/45c48cce2e2d7fbdea1afc51c7c6ad26 |
| door9  | http://MACHINE_IP/d3d9446802a44259755d38e6d163e820 |
| door10 | http://MACHINE_IP/6512bd43d9caa6e02c990b0a82652dca |
| door11 | http://MACHINE_IP/c20ad4d76fe97759aa27a0c99bff6710 |
| door12 | http://MACHINE_IP/c51ce410c124a10e0db5e4b97fc2af39 |
| door13 | http://MACHINE_IP/8f14e45fceea167a5a36dedd4bea2543 |

From the question, we get the information `they look an awful lot like a hash, don't they?`. So we try to identify the using a hash indetifier tool and the tool shows it's MD5

<img width="695" height="127" alt="image" src="https://github.com/user-attachments/assets/2ad4590c-8181-44a2-8efb-cb8946b805ed" />

Now we decrypt the first hash and it shows the value as 1 

<img width="520" height="123" alt="image" src="https://github.com/user-attachments/assets/d537ecb3-1b83-4498-99cd-ad220cdef41a" />

The above hashes are decrypted and the result shows the numbers ranging from 1-13 for all the above 13 hashes.

We can also see from the question `This could help you uncover website locations you were not expected to access.` which means we could try numbers other than 1-13. 

First we will try 14, we will encrypt this number using MD5 and get the following hash `aab3238922bcc25a6f606eb525ffdc56`

And now our URL becomes `http://MACHINE_IP/aab3238922bcc25a6f606eb525ffdc56`. This shows 404 status code

<img width="1016" height="124" alt="image" src="https://github.com/user-attachments/assets/1c9ca990-e121-4097-9f1c-6e17a747befa" />

Next we will try 15, we will encrypt this number and get the following hash `9bf31c7ff062936a96d3c8bd1f8f2ff3`

And now our URL becomes `http://MACHINE_IP/9bf31c7ff062936a96d3c8bd1f8f2ff3`. This shows 404 status code

<img width="1016" height="124" alt="image" src="https://github.com/user-attachments/assets/1c9ca990-e121-4097-9f1c-6e17a747befa" />

We didn't try 0. So now we encrypt 0 and our hash is `cfcd208495d565ef66e7dff9f98764da`

And now our URL becomes `http://MACHINE_IP/cfcd208495d565ef66e7dff9f98764da`.

<img width="847" height="222" alt="image" src="https://github.com/user-attachments/assets/a3235952-a76f-4b47-a56e-db3c6fb10e8b" />

We can see the flag : `flag{2477ef02448ad9156661ac40a6b8862e}`

__________________________________________________________________________________________________________________________________________________
