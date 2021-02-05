# Things Learnt

## Existing System
In the existing system, we use **ID – password** method  for proving our identity on Internet. It is useful in many ways but there are problems that it creates in the long run. 
* There are too many passwords to remember,
* Keeping easy to remeber passwords will make it susceptible to guessing attacks, 
* Possiblity of data breaches by hackers etc. 
* Even though using of **Identity Providers** such as Google,  helps to solve the problem of too many passwords, these providers learn certain details about us each time we use them and hence our privacy is lost. Phising technique has become common because of the fact that we are not provided an ID and password for the site we try to connect in order to verify the identity of the site.
* Unwanted correlation : collecting multiple data elements per record from a number of sites correlating details about each person. This is made possible because of the common identifier we use on every site. 
* Centralized Identifiers: here a government or a company will be the one who issues  the identifier for us. Problem is that they can revoke the identifier any time. Also there is possiblity of the central authority to be compromised. 

Paper credential model is the one we use in real world to prove our identity. It helps to prove: who issued the credential, who holds the credential and that the claims have not been altered. But with advancement in technology forging of these documents in hand and on computer is quite easy.

## Proposed System
The **verifiable credential** model is same as paper credential model. There is an authority who issues you a credential. You hold the credential in your digital wallet. When asked to prove the claims from the credential you provide a verifiable presentation to the verfier. Verifiable credential are cryptographically constructed  so that a presentation will prove four key attributes: 
* who issued the credential, 
* credential was issued to the entity presenting it, 
* claims were not tampered,
* credential has not been revoked. 

When a verifier receives a presentation, they use information from the blockchain to perform the cryptographic calculations required to prove the four attributes. Credentials are JSON docs that are constructed and digitally signed by the issuer and countersigned by the holder. For proving data , the verifiable credentials model includes a verifiable data registry.

### Self Sovereign Identity (SSI) 
SSI means the individual manages the elements that make up their identity and control the access to those crednetials digitally. The power to control the personal data resides with the individual and not any third party. A person's digital existence is now independent of any central authority - that also means that no one has the power to take away his identity.

### Decentralized Identifiers (DID)
DID are special kind of identifier created by the owner and independent of any central authority because the control of the identifier can be cryptographically proven. It looks similar to HTTP address. A new type of URL, created by anyone at anytime, globally unique, highly available, cryptographically verifiable. We can resolve a DID to obtain a **DIDDoc** which contains a public key and an endpoint for the entity controlling the DID. We can send a messgae to that entity using the endpoint. In the message, we can ask for proof of private key related to the public key.Once the proof is received, it can be verified.

### Zero Knowledge Proof (ZKP)  
ZKP allows the data to be verified without revealing what the data is. When using ZKP, prover attempts to prove something to verifier without telling anything else about that thing; so the verifier only learns about the output. 
* Selective Disclosure : The claims from verifiable credentials can be selectively disclosed, by providing only some data elements in a single presentation.

## Hyperledger Indy

Hyperledger Indy was Hyperledger's first "identity-focused" blockchain framework. It is a distributed ledger, purpose-built for decentralized identity. Developers can use the tools and libraries from Hyperledger Indy to create identity solutions that are interoperable across jurisdictions and agencies. Indy enables issuers, holders and verifiers to exchange verifiable credentials and presentations by exchange of messgaes.

## Hyperledger Ursa

Hyperledger Ursa is a shared cryptographic library that would enable people and projects to avoid duplicating other cryptographic work and hopefully increase security in the process. This project produces cryptographics packages that can be used to build higher level applications.

## Hyperledger Aries

Aries is a toolkit designed for initiatives and solutions focused on creating, transmitting, storing and using verifiable digital crednetials. Aries is all about peer to peer interactions between agents controlled by different entities.