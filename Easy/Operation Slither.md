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

[Twitter/X account link](https://x.com/V3N0MBYT3/with_replies)

[Threads account link](https://www.threads.com/@v3n0mbyt3_) 

Since Twitter/X account has numerous posts, we first see through the Threads account

I will be using mobile phone to view the posts since I would need an account to view all the content 

The threads account looks like this

![Screenshot_2026-03-12-10-29-31-03_b86672daa061159f52c1a3195c773d05](https://github.com/user-attachments/assets/a4213500-40d1-4fb2-a2c2-30eba9e5e063)

We read through the posts and comments and find two comments peculiar. One is `I still can't believe they are not stil aware of us for weeks` and other is `It's time to harvest soon!`

[Post Link](https://www.threads.com/@v3n0mbyt3_/post/C6Bgdo9PeFR)

Both of these sentences point to these bad actors inside TryTelecomMe's network and harvesting can mean data harvesting

![Screenshot_2026-03-12-10-40-01-20_b86672daa061159f52c1a3195c773d05](https://github.com/user-attachments/assets/dfd9be63-61b6-49d2-b1fb-88b975715fea)

At the bottom of the same thread, we can see a base64 decoded text `VEhNe3NsMXRoM3J5X3R3MzN0el80bmRfbDM0a3lfcjNwbDEzcyF9`

![Screenshot_2026-03-12-10-40-01-20_b86672daa061159f52c1a3195c773d05(1)](https://github.com/user-attachments/assets/2477d8a0-5d15-412d-b9c8-9035e91de3bb)

We use [Cyberchef](https://gchq.github.io/CyberChef/) and decode the text

<img width="1050" height="233" alt="image" src="https://github.com/user-attachments/assets/4d67dc16-1414-4d30-92d8-6cdc0c063733" />

Decoded text: `THM{sl1th3ry_tw33tz_4nd_l34ky_r3pl13s!}`

**Answer the questions below**

1. **_Aside from Twitter / X, what other platform is used by `v3n0mbyt3_`? Answer in lowercase._**

Answer: `threads`

**Explanation:**

We did find a threads account with the username `v3n0mbyt3_` and there's also an Instagram profile for this user but we find nothing on their [Instagram](https://www.instagram.com/v3n0mbyt3_/) account. Sine we have found some useful information on Threads account, the answer to this question will be `threads`

2. **_What is the value of the flag?_**

Answer: `THM{sl1th3ry_tw33tz_4nd_l34ky_r3pl13s!}`

**Explanation:**

We did decode the base64 text and got our flag


______________________________________

**Task 2: The Sidekick**

Below the same thread from the previous task, we see another peculiar comment `Hidden content ------------------------` from the account `a2208016` and we can also see some accounts bidding.  

[Post Link](https://www.threads.com/@a2208016/post/DITXXbBManN?xmt=AQF0AFt_WLEyqwkDIk86dzZN5RgMpqgP6kscQHFHE8jnvQ)

This points to accounts trying to buy harvested data through cryptocurrency. 

Since we already have two operator's accounts: `v3n0mbyt3_` and `_myst1cv1x3n_` 

[Threads account of second operator](https://www.threads.com/@_myst1cv1x3n_)

Now we try to find other accounts associated with `_myst1cv1x3n_`

<img width="632" height="619" alt="image" src="https://github.com/user-attachments/assets/f79a33c9-748a-488f-b94b-7581ba10d498" />

We can see that this second operator has an [Instagram account](https://www.instagram.com/_myst1cv1x3n_/)

<img width="747" height="255" alt="image" src="https://github.com/user-attachments/assets/71e837fd-c7ef-483b-a0d5-e1909bf3586f" />

We try to look through their posts and come across a reel with some calming music 

[Link to the reel](https://www.instagram.com/_myst1cv1x3n_/reel/C6BuP1CNMCI/)

![Screenshot_2026-03-12-11-37-43-43_1c337646f29875672b5a61192b9010f9](https://github.com/user-attachments/assets/70263792-fed4-4d91-a314-86b1bae7c3f0)

From the reel description, we see a link to [Soundcloud](https://soundcloud.com/v1x3n-195859753/prototype1)

![Screenshot_2026-03-12-11-37-43-43_1c337646f29875672b5a61192b9010f9(1)](https://github.com/user-attachments/assets/a7e1950c-3568-4898-8b67-b4df56bfdbdf)

We visit this link and open their profile

<img width="1337" height="907" alt="image" src="https://github.com/user-attachments/assets/c3eb2bc5-2d29-4f6a-a4b4-69937c24e7f1" />

<img width="1318" height="861" alt="image" src="https://github.com/user-attachments/assets/feeac204-a56f-4552-a1ba-4761bd46a64e" />

[SoundCloud Profile](https://soundcloud.com/v1x3n-195859753)

We find a peculiar recording of their operation

<img width="857" height="216" alt="image" src="https://github.com/user-attachments/assets/d770a259-cf3f-4656-8460-c365e084afe0" />

[Link of the Operation Recording](https://soundcloud.com/v1x3n-195859753/prototype2)

After playing this recording, we find that they have a github account and they also mention on how they bypassed the defences

And we can see another base64 encoded text below this recording `VEhNe3MwY20xbnRfMDBwczNjX2Yxbmczcl9tMXNjbDFja30=`

<img width="866" height="350" alt="image" src="https://github.com/user-attachments/assets/08021ce2-7065-4c3a-bba9-0465e360bace" />

We decode it with [CyberChef](https://gchq.github.io/CyberChef/) and get the decoded text

<img width="1540" height="227" alt="image" src="https://github.com/user-attachments/assets/bf801a12-4f5f-4874-9171-702e2a03560f" />

Decoded text: `THM{s0cm1nt_00ps3c_f1ng3r_m1scl1ck}`

**Answer the questions below**

1. **_What is the username of the second operator talking to v3n0mbyt3 from the previous platform?_**

Answer: `_myst1cv1x3n_`

**Explanation:**

We labelled the person behind the account `_myst1cv1x3n_` as the second operator because of their communication with `v3n0mbyt3_`

2. _**What is the value of the flag?**_

Answer: `THM{s0cm1nt_00ps3c_f1ng3r_m1scl1ck}`

**Explanation:**

We got a base64 encoded text from soundcloud and we decoded it and got our flag

___________________________________________________________________

**Task 3: The Last Operator**

We can see this recording which we found from the previous task is being liked by some people and can one of them be the third operator? Let's see

<img width="859" height="128" alt="image" src="https://github.com/user-attachments/assets/c5c27055-0d3f-4a48-8228-ae5a6c71752b" />

<img width="1291" height="456" alt="image" src="https://github.com/user-attachments/assets/b1d6df36-5288-40ab-9855-3fd89fc19b77" />

The account `sh4d0wF4NG` looks suspicious but we find nothing in their soundcloud account

<img width="1297" height="776" alt="image" src="https://github.com/user-attachments/assets/1acba620-ac18-423e-a7f7-7affda9d72fd" />

But the suspicion raises that the person behind this could be the third operator, but why? Because we can see they are following `_myst1cv1x3n_` on soundcloud

[sh4d0wf4ng's SoundCloud account](https://soundcloud.com/sh4d0wf4ng)

<img width="384" height="252" alt="image" src="https://github.com/user-attachments/assets/26de47a2-24d2-41e0-91e5-6bd499606ac1" />

We search the username `sh4d0wF4NG` and we find a GitHub account

[sh4d0wf4ng's GitHub](https://github.com/sh4d0wF4NG/red-team-infra)

<img width="686" height="143" alt="image" src="https://github.com/user-attachments/assets/478811ee-e70f-431f-8c19-d32620f82dfa" />

We go through the each file of this repo and other repos of this accout and find nothing

<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/4dd79fd9-5506-42b3-ae1b-77f1038f7f97" />

But we can see the previous commits of this account 

<img width="1845" height="956" alt="image" src="https://github.com/user-attachments/assets/a0a00d11-ee48-4c9c-ae14-fe829e058d06" />

We open this particular commit

<img width="585" height="88" alt="image" src="https://github.com/user-attachments/assets/1460ab24-7dad-4014-a23f-08d477c740e2" />

[Link to find the commit and encoded text](https://github.com/sh4d0wF4NG/red-team-infra/commit/78de1f17c45b994e97b8629aa7e5f42c31a0e7f7)

We scroll down and see base64 encoded text : `VEhNe3NoNHJwX2Y0bmd6X2wzNGszZF9ibDAwZHlfcHd9`

<img width="1465" height="744" alt="image" src="https://github.com/user-attachments/assets/f0bae532-e3a4-4d46-a96d-45602d312dac" />

We use [Cyberchef](https://gchq.github.io/CyberChef/) and decode the text

<img width="979" height="220" alt="image" src="https://github.com/user-attachments/assets/bd810fa9-1743-4035-91c6-f7abf41c430a" />

Decoded Text: `THM{sh4rp_f4ngz_l34k3d_bl00dy_pw}`

**Answer the questions below**

1. **_What is the handle of the third operator?_**

Answer: `sh4d0wF4NG`

**Explanation:**

Since this account was following `_myst1cv1x3n_` on soundcloud and liked their recording

2. **_What other platform does the third operator use? Answer in lowercase._**

Answer: `github`

**Explanation:**

We did find GitHub account of `sh4d0wF4NG`

3. **_What is the value of the flag?_**

Answer: `THM{sh4rp_f4ngz_l34k3d_bl00dy_pw}`

**Explanation:**

On `sh4d0wF4NG` GitHub's account, we found a previous commit with a base64 encoded text which was our flag

____________________________________________________________________________________________
