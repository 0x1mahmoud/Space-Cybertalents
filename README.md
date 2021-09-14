# Cybertalents Space Web Security Challenge
 
 ### pts 200, Hard
 
 
 
 here we go...
 
 after clicking this challenge link http://ec2-35-158-236-11.eu-central-1.compute.amazonaws.com/space/
 
**you will see this page**

![Image of mahmoudashraf1344](https://github.com/0x1mahmoud/Space-Cybertalents/blob/main/img/img1.png)

---------------------------------------------------------------------------------------------------------------------

### so i'll go to brute force the files in this web by Gobuster or dirb etc....

![Image of mahmoudashraf1344](https://github.com/0x1mahmoud/Space-Cybertalents/blob/main/img/img2.png)


### and here we go i find there's robots.txt

![Image of mahmoudashraf1344](https://github.com/0x1mahmoud/Space-Cybertalents/blob/main/img/img3.png)


### let's open it

![Image of mahmoudashraf1344](https://github.com/0x1mahmoud/Space-Cybertalents/blob/main/img/img4.png)

### We see there're double auditor 
so **auditor/auditor**

---------------------------------------------------------------------------------------
i don't know what is this and how to use and the webapp only have robots.txt
so i try to type login.php and i go it

![Image of mahmoudashraf1344](https://github.com/0x1mahmoud/Space-Cybertalents/blob/main/img/img5.png)

i try to brute force username and password and there's nothing
but i tryied to type **username: auditor password: auditor**
like this...
![Image of mahmoudashraf1344](https://github.com/0x1mahmoud/Space-Cybertalents/blob/main/img/img6.png)

and i've logged in and i'm in auditor place we need to be admin
so let's opne up burp suite to see the request and response when i logged in

![Image of mahmoudashraf1344](https://github.com/0x1mahmoud/Space-Cybertalents/blob/main/img/img7.png)

## we see there a signature & session
it's **hash length Attack**

### go and download hash_extender

![Image of mahmoudashraf1344](https://github.com/0x1mahmoud/Space-Cybertalents/blob/main/img/img8.png)
