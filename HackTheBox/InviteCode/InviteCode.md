
# Hack The Box – Invitation Code Writeup

![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/HackTheBox/InviteCode/pic/inv0.png)

How to Access ?
Hackthebox.eu doesn’t allow you to register. The only way to sign up is by having an insider to provide you with an invite code or hack your way in.
I don’t have someone to provide me an invite code so I have to hack me way in.
I start off by analyzing the source code of the Invite Code form, where I find an interesting javascript inviteapi.min.js

 ![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/HackTheBox/InviteCode/pic/inv1.png)

you will have to take at all the js files present there and there you will see a js file named inviteapi.min.js
and in that js file you will see that there is a function named: makeInviteCode() this function actually 
make/generates your required invite code

![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/HackTheBox/InviteCode/pic/inv2.png)

you will get an ROT13 encrypted code as a response in the above POST request
Now decrypt that ROT13 code using any online decoder
https://cryptii.com/pipes/rot13-decoder

![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/HackTheBox/InviteCode/pic/inv3.png)

After decrypt ROT13 Code hence make a POST request to the endpoint mentioned in the /function/api/invite/generate  using curl or any other online tool to make a POST request 
the invite code generated tracks your IP address hence you will not get the correct code for your IP if you make the POST request using any other online tool:
post request on browser:
 
![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/HackTheBox/InviteCode/pic/inv4.png)
 
curl -XPOST https://www.hackthebox.eu/api/invite/generate 
echo R0hIWEMtS1NVWEstVEZCTUctQlZUSEctTUFKSU4= | base64 –decode

![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/HackTheBox/InviteCode/pic/inv5.png)

After decrypt base64 code we have the self invite code  

![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/HackTheBox/InviteCode/pic/inv6.png)

Let’s Capture The Flag’s
Old Writeups source : https://github.com/MrMugiwara/WriteupsCTF 
