# SSL/TSL for humans
![d1dd3fb6.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\d1dd3fb6.png)

![a00ec4c3.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\a00ec4c3.png)

## A human public private and asymmetric key crptography example

There's a message
put message into safe
lock using public key
Only the recipient has private key to open the safe

Now we can deliver the safe on any unreliable connection and it will still arrive safe

## A human RSA example
![0405ecba.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\0405ecba.png)

![b54f4b37.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\b54f4b37.png)

![59b9298e.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\59b9298e.png)

![dcd8e218.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\dcd8e218.png)

![2572c5e9.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\2572c5e9.png)

## A Secure communication
![483cecfe.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\483cecfe.png)

![1f1a45b1.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\1f1a45b1.png)

![7bd7d763.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\7bd7d763.png)

** If you do not use https, you will be able to see all the info in logs for even local server**

## Signed Certificate
A certificate contains :-
* Serial Number
* Subject
* Validity
* Usage
* public key
* fingerprint algo
* fingerprint
License is like driving license
e.g. number, subject is me, it has validity, no public key though

## What is self signed certificate
Now self written driving license are no good
hence we need
* Signature Algo
* Singature
Basically someone certifiying I am allow to drive **digital certificate**
Now we need Signature Algo for that
e.g. **public/private cryptography**
* Issuer

e.g. I will use my private key to put signature in safe then anyone having public key can open and be sure that I was the one who closed the safe and hence the signature is correct

** more formally**
![cc802b76.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\cc802b76.png)

## Who is going to sign certificate
** Certificate authotiries**
![cf63e4be.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\cf63e4be.png)
A certificate has been issued to me and a certifies that i own as a certain public key and its my responsibility that I key the private key to myself and I don't lose it

## Delegate trust
when certificate authorities trust each other

![876512c6.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\876512c6.png)

There are different John's in our browsers and OS
![4e2b4d6a.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\4e2b4d6a.png)
![435b9e03.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\435b9e03.png)

169 Johns

Now these are introduced by our browsers since they keep the list and subsequent trusted parties

Now these authorities has very tight securities and key ceremonies

![2c212831.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\2c212831.png)

These key ceremonites have cameras, notary, randomness 

## Extended validation certificate
![f803931c.png](:storage\e871cab9-fb76-4377-8fc4-3080bdbab3a8\f803931c.png)

Now lets say someone copies the user interface of bank and have a domain name similar and a certificate issued to him. We will be compromised because of typo in address room

Now along the address bar ** you will see the name ING Bank** Now that tells us this certificate has been issued to a **legal entity** named ING Bank

## Some useful commands
curl -v -k address
-v -> verbose
-k -> if the certificate is not in my trust list, still continue

## For troubleshooting certificate issues
**OpenSSL**
openssl s_client -showcerts -servename address -connect address:443

multiple servername in case webserver is running multiple domain name

## Troubleshoot protocols, ciphers
nmap --script ssl-enum-ciphers -p 443 address

## JVM settings
-Djavax.net.ssl.trustStore=file
-Djavax.net.ssl.trustStorePassword=changeit

**Truststore** is a file in local, which basically has certificate developer willing to trust
In case encrypted, need a password to decrypt

-Djavax.net.ssl.keyStore-file
keystore contains public and or private keys

-Djavax.net.ssl.keyStorePassword=changeit

## If still need troubleshooting
-Djavax.net.debug=ssl[:flag]
Include debug logging for TLS handshake and connections

Additional flags:

record, session, sessioncache, pluggability, plaintext, handshake defautctx, keymanager, data, packet, keygen, sslctx, trustmanager, verbose    

## References
[YouTube](https://www.youtube.com/watch?v=u6bLCfU3iSk)