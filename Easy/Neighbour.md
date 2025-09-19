Link: https://tryhackme.com/room/neighbour

<img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/fbcb6da6-012f-43ce-94b1-ed25d728ff12" />

Check out our new cloud service, Authentication Anywhere. Can you find other user's secrets?

**Task 1: Neighbour**

Check out our new cloud service, Authentication Anywhere -- log in from anywhere you would like! Users can enter their username and password, for a totally secure login process! You definitely wouldn't be able to find any secrets that other people have in their profile, right?


Access this challenge by deploying both the vulnerable machine by pressing the green "Start Machine" button located within this task, and the TryHackMe AttackBox by pressing the  "Start AttackBox" button located at the top-right of the page.

Navigate to the following URL using the AttackBox: http://MACHINE_IP

Check out similar content on TryHackMe:

  - [IDOR](https://tryhackme.com/room/idor)

**Answer the questions below**

1. _Find the flag on your neighbor's logged in page!_

Answer: `flag{66be95c478473d91a5358f2440c7af1f}`

**_Explanation:_**

We visit the MACHINE_IP and see a login page

<img width="1337" height="529" alt="image" src="https://github.com/user-attachments/assets/f7d9cbb1-37b8-4fb8-82eb-53e5217260eb" />

Now we can see that there's a guest account which can be used and we press Ctrl+U 

And now we have credentials for guest user

<img width="1039" height="654" alt="image" src="https://github.com/user-attachments/assets/dd8b7502-f944-4470-86b8-e4f8e6c61f5e" />

We login using the above creds

<img width="432" height="381" alt="image" src="https://github.com/user-attachments/assets/fef8ea22-3f24-4a92-bbe5-21768fa7cf9e" />

And our guest page appears like this

<img width="1919" height="248" alt="image" src="https://github.com/user-attachments/assets/3bb333b7-c30d-4ffe-8c4c-fa0111604347" />

Now in the URL we see a parameter called `user=guest` 

`http://10.10.204.166/profile.php?user=guest`

Now we try to change the user to admin `http://10.10.204.166/profile.php?user=admin`

<img width="344" height="39" alt="image" src="https://github.com/user-attachments/assets/1fe5a744-2ccb-4662-aacb-2c3b9f0fb05a" />

And now we can see the flag

<img width="1915" height="255" alt="image" src="https://github.com/user-attachments/assets/fd8f7807-104f-4ee4-aa93-931db2a09551" />

---
