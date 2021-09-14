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

after you've installed it type this command
`./hash_extender --data "user=auditor&role=auditor" --secret 38 --append admin --signature 9cdc8cbee716e38a1549f52a797fc4466e826097`

you have to know this command what it means....

![Image of mahmoudashraf1344](https://github.com/0x1mahmoud/Space-Cybertalents/blob/main/img/img9.png)

so i got a new **New signature: e2467f09b8e23ffee8c16196222dc25995044589**
and aslo **cookies New string: 757365723d61756469746f7226726f6c653d61756469746f7280000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001f861646d696e**

## i'll take them and put them in

**Cookies= 757365723d61756469746f7226726f6c653d61756469746f7280000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001f861646d696e**
**signature= e2467f09b8e23ffee8c16196222dc25995044589**

![Image of mahmoudashraf1344](https://github.com/0x1mahmoud/Space-Cybertalents/blob/main/img/img10.png)



after refreshing the page you'll be in the admin place view the source code you see the **flag**
## Have fun, Enjoy, bye bye.....
