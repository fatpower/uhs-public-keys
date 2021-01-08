# Public encryption keys of UHS Members
This repository purpose is to collect public keys from each organization member. With the public key members identification could be verificated and could be used for encryption purposes. 

## Main advantages 
* Organization members can identify even if their account is compromised or lost. This could happen easily if members have longer breaks. 
* Organization secrets would not leak even if discord / github or other platform get compromised
* It's freaking awesome and cost nothing

## Directory structure
* /docs - Directory contains HOWTO documentation to create the private-public key pair
* /members - Directory contains organization members public keys
* /3rd-party - Directory contains other trusted keys such as service accounts, bots.

## Basic principle
Each organization member generates their own private-public key pair. Private key is a secret one and should be stored in a secure place and never shared with anyone.
Public keys will be shared between org members via this repository. Each member can sign other members keys and release a signed version to this repository. This method is called a Web of trust (WoT).  By signing keys it is easy to see who else is trusting the key and it is easier to make choices to trust or not to trust, good example is when new people are joining the organization. 

## Encryption
Public key can be used to encrypt files which are not possible to open any other key then private key from the same key pair. In practice this means if you have someone public key you could make a message what nobody else can read.

Encrypted messages could be encrypted with multiple public keys, this allows to share organization resources between members without worry that the message platform (example discord) itself gets compromised.

## Good to know
* Public key is public, it can be shared to anyone!
* Private key is secret, if you lose it you can not decrypt messages or make id. So make backup to some offline media like usb stick and store it in a secure place.
* DO NOT SHARE PRIVATE KEY EVER
* There is no known methods to compromise or decrypt PGP messages* Signing and exporting other people public keys is a announcement that you trust the private key (The person who owns it)

## TODO
* Make challenge method to organization bot to make PGP based identification
