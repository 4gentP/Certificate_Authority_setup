# Certificate_Authority_setup

This report focuses on creating an independent root Certificate Authority (CA), eliminating the need for commercial CA involvement and financial transactions. Root CAs are pivotal in issuing digital certificates, certifying ownership of public keys. While commercial CAs like VeriSign dominate, this project enables us to become a self-reliant root CA. This empowers us to generate self-signed certificates for various purposes, without external CA dependence. Root CA certificates, unconditionally trusted and preloaded in software, play a crucial role in digital security. This initiative facilitates the creation of self-signed root CA certificates, enhancing our ability to issue certificates securely and independently.

 ![image](https://github.com/4gentP/Certificate_Authority_setup/assets/69531842/8b80f534-c37c-4b9d-8593-18984824b7c4)

Initially opening PKILabServer.com, throws an error as the certificate for the webpage is not a trusted certificate under the existing CA embedded in Firefox.

 ![image](https://github.com/4gentP/Certificate_Authority_setup/assets/69531842/71008528-089f-49c5-beb9-7c9224319804)
After adding our own CA into Firefox the webpage loads as thought it is a secure website. 

 ![image](https://github.com/4gentP/Certificate_Authority_setup/assets/69531842/a93c8189-59f0-4775-8fcc-7dec9df4bc5f)
Using the local host again gives an invalid certificate issue as it is not recognized as part of our or any CA.

 ![image](https://github.com/4gentP/Certificate_Authority_setup/assets/69531842/cbc9b6f7-214c-4bb0-975b-09e2cc7559e1)
Changing a byte of server.pem makes the server certification invalid, this disables us from activating the CA server.
