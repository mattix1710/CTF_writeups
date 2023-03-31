# who is it

![type_forensics](https://img.shields.io/badge/type-forensics-red)
![sub_type_email](https://img.shields.io/badge/sub_type-email-orange)
![level_easy](https://img.shields.io/badge/level-easy-green)
![points_100](https://img.shields.io/badge/points-100-blue)

## Intro
> Someone just sent you an email claiming to be Google's co-founder Larry Page but you suspect a scam.
> Can you help us identify whose mail server the email actually originated from?
> Download the email file [here](https://artifacts.picoctf.net/c/499/email-export.eml). Flag: picoCTF{FirstnameLastname}

## Solution
* After opening the file we can see raw e-mail text with all the header content. 
* We have to find the name of the owner of outgoing server!
* We need to focus on IPv4 address from **Received** section
* In verse 29 we can find line: `Received: from mail.onionmail.org (mail.onionmail.org. [173.249.33.206])`
* Challenge title indicated that we could use `whois` tool
  * So we can use all the information and look up `whois 173.249.33.206` and then we are getting the final list of informations, which includes the name of the servers owner!