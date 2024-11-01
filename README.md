# h2-Pubkey

## Read and summarize (with some bullet points)
**€ Schneier 2015: Applied Cryptography: Chapter 2 - Protocol Building Blocks, sections
2.5 Communications Using Public-Key Cryptography
2.6 Digital Signatures
2.7 Digital Signatures With Encryption**

I was not able to do this task as assigned. The the book selected for reference material as it was not available through the web site. Despite multiple attempts to start trial on https://www.oreilly.com/start-trial/, the site continued to fail my registration.

Luckily the heroes of Internet Archive delivered some version of the book and my takeouts are the following. The text was super difficult for me to understand so my summary is bit lacklustery. 

2.5 
* Public-key cryptography is a way to encrypt sensitive messages. 
* Two Keys are created in publi-key encryption: public and private. Anyone with public key can encrypt the message but only private key can decrypt the message.
* These two keys have different levels of protection: public is simple and private is complex.
* Hybrid cryptosystems are practical implementations of public-key cryptography and can be used to ensure more secure ways to encypt messages. The secret of protection is keys that are valid for certain period and will change after used.
* Merkle’s Puzzles is an implementation of a public-key cryptosystem model. It allows two parties to share secrets by messaging. This can happen even though the parties may not have secrets in common beforehand.

2.6
* A digital signature is an electronic stamp of authentication. Digital signatures are used for encrypted of digital information such as email messages, macros, or electronic documents.
* There are multiple examples on how these signatures work and encypt content.
* Digital signatures can be forged/staged but with technology it is made more difficult.

2.7
* To achieve best level of security, digital signatures can be combined with public-key cryptography. 

Would is be possible for us to have materials that are accssible without having to log in to whatever system? From cyber security perspective, it is not the best idea to have to give out your information to whatever sites.

2.8 Random And Pseudo-Random-Sequence Generation

* Random-number generators don't produce a random sequences as that is impossible.
* Pseudo-random-sequence generators work and those are possible for computers. Pseudo-random sequence looks random enough so it passes verifications.
* Cryptographic applications work with pseudo-random-sequence generators. Pseudo-random-sequence must also be secure enough and resistant to break-ins.


**€ Rosenbaum 2019: Grokking Bitcoin:
Chapter 2. Cryptographic hash functions and digital signatures:
Digital signatures (8 sections, from "Typical use of digital signatures" to "Private key security")**

I was not able to do this task as assigned. The the book selected for reference material as it was not available through the web site. Despite multiple attempts to start trial on https://www.oreilly.com/start-trial/, the site continued to fail my registration..

Luckily, Kalle Rosenbaum seems to have added his book into Github: https://github.com/kallerosenbaum/grokkingbitcoin/blob/master/ch02-hash-functions-and-signatures.adoc  so I was able to access the material to certain extent?

Points from the article:
* Typical use of digital signatures descibes the actions related to using digital signatures. The process works so that private key ans public keys are created for signed feature is. Then public key is handed over to receiver. Then, signed feature is protected with private key. Receiver then accesses the signed feature by using public key. If ther has been chnages in signature, public key will fail.
* Improving cookie token security describes how to cookies should be used to increase security though key pairs and how the process works.
* Private key security descibes how cookie tokens are managed through private key and how losing the key would be detrimental. The text also thinks about differences on storing private key (online vs offline, clearteaxt vs encryption and splitting the key or storing it as a whole.

**Karvinen 2023: PGP - Send Encrypted and Signed Message - gpg**

* Article exlains how to send enctypted and signed messages.

* I had hard time reading the article. I did not really understand where to start without grapic interface so I will skip the tasks related to the article. I apologize for this.


## Pubkey today. Explain how you have used public key cryptography today or yesterday, outside of this homework. In addition to naming the system, identify how different parties use keys in different steps of the system. (Answering this question likely requries finding sources on your own. This subtask does not require tests with a computer.)

I'm my company's Jira admin and superuser in addition to my other roles. In this admin work, I have sometimes used public keys to integrate our Jira instance with collaborator's Jira/other tools instances. The process of using public keys has been quite simplistic: Jira admin interface supports use of public keys and has comprehensive guidelines on how to perform this task.

The process is simple enough: 
1. Key-pair is generated. 
2. Public key is extracted in PEM format
3. Public Key is moved to text editor
4. Finally, key is copied into JIRA
(Atlassian)

Recently, Jira has encouraged the use of API's to do integrations so public keys are not that often used anymore. 

## Messaging. Send an encrypted and signed message using PGP, then verify and decrypt it. (You can use folders to simulate users, or use two computers or two different OS users. Don't use Tero as a name of any party, unless that's your given name.)

* I'm skipping this task. This task proved to be too hard for me. I have no issues with using graphical interfaces such as Outlook encryption or even Jira encryptiontion which is more light-weight but my brain does not wrap aroud this task. Sorry about that.

## Other tool. Encrypt a message using a tool other than PGP. Explain how different parties use different keys at different stages of operation. Evaluate the security of the tool you've chosen.

Using Outlook encryption to demonstate practical, real-life encyption example.

Outlook has built-in encryption fetures. Encrypting an email message in Outlook means it's converted from readable plain text into scrambled cipher text. Only the recipient who has the private key that matches the public key used to encrypt the message can decipher the message for reading. (Micorosoft)

Outlook encryption is very simple.
* from graphical interface, Options should be selected, and then Encrypt.
* Outlook requires user to select encryption type such as Encrypt-Only or Do Not Forward. Do Not Forward means that message stays encrypted within Microsoft 365 and can’t be copied or forwarded. Encrypting means that the message stays encrypted and doesn’t leave Microsoft 365. If recipient has other email client, temporary passcode can be downloaded to open message and contents. Default setting uses Outlook.com's opportunistic Transport Layer Security (TLS) to encrypt the connection with a recipient’s email provider.
* Compose email, add contents, ensure that encyrption is on. Then choosing Send will send the encyrpted message to other people. (Microsoft)  

* Outlook encyrption is very user-friendly and simple to use. It could have even better graphical interface and it could be even smoother visually (as well as more popping so that it would be easier to find and thus use) but it does it's thing and foes it very well. Microsoft also states that they use "some of the strongest, most secure encryption protocols available to provide barriers against unauthorized access to customer data". Microsoft states that they use Internet Protocol Security (IPsec) and Transport Layer Security (TLS) to perform encryption. Micorosft also has their own security standards such as Public Key Infrastructure Operational Security Standard. (Microsoft Encryption)


## Eve and Mallory. In many crypto stories, Eve is a passive eavesdropper, listening on the wire. Mallory maliciously modifies the messages. Explain how PGP protects against Mallory and Eve. Be specific what features, which use of keys and which flags in the command are related to this protection. (This subtasks does not require tests with a computer)

* PGP prevents Eve from eavesdropping as it protects data with random key. Without random key, Eve cannot access the data.  I don't undarstand the flag thing so not guessing.

* PGP blocks Mallory from modifying data. Modifying data without private key to decrypt it, modify and encrypt is not possible. If data is protected by private key, I think that Mallory is not able to manage this data.  With public key, Mallory can still access the data but cannot change it. I don't undarstand the flag thing so not guessing.


## Password management. Demonstrate use of a password manager. What kind of attacks take advantage of people not using password managers? (You can use any password manager, some examples include pass and KeePassXC.)

iPhone has inbuilt password manager. It is pretty simple to use: It stores passwords from various websites and mobile applications and gives user the access to these passwords through PIN code or biometrics (FaceID). 

How it works:
1. Open the Passwords app through settings
2. Unlock with Face ID or Touch ID, or enter passcode.
3. Select the system, application or website password is needed for

iPhone also suggests strong passwords that it stores into password manager and will fill in your password information onto websites after you confirm that you want it to show your passwords (Again, PIN or biometrics is required to confirm this).

iPhone Password is not as advaced as for example 1Password or Keepass, but it is good everyday application that is easily accessible and works seamlessly with regular everyday phone user experience. Anbd it is not less safe than more refined solution, as according to Apple, the Passwords app uses AES-256 bit and end-to-end encryption to keep stored credentials secure. (D'Andrea, A)

** What kind of attacks take advantage of people not using password managers?** 

* People who use too weak passwords (e.g. passwords that are rememberable for human mind), experience more issues as cybercriminals can crack weak passwords in seconds. If the password is more complex, containing numbers, symbols and uppercase and lowercase letters, the time needed to break it jumps to 400 years.(Kate O'Flaherty)
* Password manager apps can resolve this problem by creating long and complex credentials for various services. (Kate O'Flaherty)
* Password managers also remove the theart that is using the same password in multiple services. If same password is used in multiple services, that makes it easier for hackers. It is better to use passwrod manager that is being hacked into than to have multiple account with same password. If the phone PIN is too easy or biometrics are not in use, then of course security level of the Passwords tools is weaker. (Kate O'Flaherty)
* Apple Password is only available for Apple devices so that can be one preventing measure if user is mixed user (Windows PC, Android tablet and Apple phone).

* Different attack types towards users not using password managers are for example:
  **Bruteforcing something open. It is easier if the password is not complex. (Onelogin)
  **Dictionary attack in which attacker tries to use common words to open your account. (Onelogin)
  ** Credential stuffing where attackers try to use same passwords for multiple sites. (Onelogin)
  ** Normal Phishing done with traditional tools such as emails, false links and other. (Onelogin)  
  

## Refer to sources. Verify each homework report (this and the earlier ones) refers to sources. Every homework report should refer to this task page. It should also have references to any other source used, such as web pages, LLMs, man pages, other reports... References are mandatory, and must be present in every report. (This subtask does not need a report, you can just do it and write "Done." as the answer for this subtask.)

Will do referrals. o7

## Sources

Atlassian. 7 June 2017. How to generate public key to application link 3rd party applications 
https://confluence.atlassian.com/jirakb/how-to-generate-public-key-to-application-link-3rd-party-applications-913214098.html 

Kate O'Flaherty. 19 Mar 2022. Not using a password manager? Here’s why you should be…
https://www.theguardian.com/technology/2022/mar/19/not-using-password-manager-why-you-should-online-security

Onelogin. Six Types of Password Attacks & How to Stop Them
https://www.onelogin.com/learn/6-types-password-attacks

Microsoft. Learn about encrypted messages in Outlook.com
https://support.microsoft.com/en-us/office/learn-about-encrypted-messages-in-outlook-com-3521aa01-77e3-4cfd-8a13-299eb60b1957 

Microsoft. 20 March 2024. Encryption in the Microsoft cloud
https://learn.microsoft.com/en-us/purview/office-365-encryption-in-the-microsoft-cloud-overviewhttps://learn.microsoft.com/en-us/purview/office-365-encryption-in-the-microsoft-cloud-overview 

Ashley D'Andrea. 21 October 2024 Is Apple’s Passwords App Safe?
https://www.keepersecurity.com/blog/2024/10/21/is-apples-passwords-app-safe/
