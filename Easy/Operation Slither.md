Link: https://tryhackme.com/room/operationslitherIU

**Task 1: The Leader**

We are given a post in the challenge 

```
Full user database TryTelecomMe on sale!!!

As part of Operation Slither, we've been hiding for weeks in their network and have now started to exfiltrate information. 
This is just the beginning. We'll be releasing more data soon. Stay tuned!

@v3n0mbyt3_

---
```

We take the username `v3n0mbyt3_` and search if any social profiles match this username

We find that this username is also associated with one threads and Twitter/X accounts

<img width="396" height="118" alt="image" src="https://github.com/user-attachments/assets/930b6c68-2dec-405f-908b-e86befa46caf" />

<img width="481" height="115" alt="image" src="https://github.com/user-attachments/assets/b683e8fb-b5b0-41a3-8178-c3ac520ed5d6" />

Since Twitter/X account has numerous posts, we first see through the Threads account

I will be using mobile phone to view the posts since I would need an account to view all the content 

The threads account looks like this

![Screenshot_2026-03-12-10-29-31-03_b86672daa061159f52c1a3195c773d05](https://github.com/user-attachments/assets/a4213500-40d1-4fb2-a2c2-30eba9e5e063)

We read through the posts and comments and find two comments peculiar. One is `I still can't believe they are not stil aware of us for weeks` and other is `It's time to harvest soon!`

Both of these sentences point to these bad actors inside TryTelecomMe's network and harvesting can mean data harvesting

![Screenshot_2026-03-12-10-40-01-20_b86672daa061159f52c1a3195c773d05](https://github.com/user-attachments/assets/dfd9be63-61b6-49d2-b1fb-88b975715fea)

At the bottom of the same thread, we can see a base64 decoded text `VEhNe3NsMXRoM3J5X3R3MzN0el80bmRfbDM0a3lfcjNwbDEzcyF9`

![Screenshot_2026-03-12-10-40-01-20_b86672daa061159f52c1a3195c773d05(1)](https://github.com/user-attachments/assets/2477d8a0-5d15-412d-b9c8-9035e91de3bb)

We use [Cyberchef]() and decode the text

<img width="1050" height="233" alt="image" src="https://github.com/user-attachments/assets/4d67dc16-1414-4d30-92d8-6cdc0c063733" />

Decoded text: `THM{sl1th3ry_tw33tz_4nd_l34ky_r3pl13s!}`

**Answer the questions below**

1. **_Aside from Twitter / X, what other platform is used by `v3n0mbyt3_`? Answer in lowercase._**

Answer: `threads`

**Explanation:**

We did find a threads account with the username `v3n0mbyt3_`

2. **_What is the value of the flag?_**

Answer: `THM{sl1th3ry_tw33tz_4nd_l34ky_r3pl13s!}`

**Explanation:**

We did decode the base64 text and got our flag


______________________________________
