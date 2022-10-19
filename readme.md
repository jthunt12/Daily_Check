# Daily_Check -- SSL Certificate Audit Playbook 

Cert_Check is a playbook that performs a handshake with a list of URLs through specified ports.

# community.crypto

community.crypto.get_certificate module will be required to create a secure connection and return information about a certificate. The requirements for this module are as follows:

- python >= 2.7
- cryptography >= 1.6

Installation:

```
ansible-galaxy collection install community.crypto
```

Check:

```
ansible-galaxy collection list
```
Vars are stored in ~/roles/vars/main.yml

By default the cert info is printed in "~/roles/.cert_diag.txt" this will need to be updated in the playbook depending on where the playbook is being ran.

# Example output from ".cert_diag.txt"

```
Daily Check Summary

 - NAME/ URL: www.redhat.com
   EXPIRATION: 2023-09-15 23:59:59 --> 332 days
   ISSUER: DigiCert SHA2 Extended Validation Server CA

 - NAME/ URL: www.ibm.com
   EXPIRATION: 2023-08-25 23:59:59 --> 311 days
   ISSUER: DigiCert TLS RSA SHA256 2020 CA1

 - NAME/ URL: www.vmware.com
   EXPIRATION: 2023-05-23 23:59:59 --> 217 days
   ISSUER: DigiCert TLS RSA SHA256 2020 CA1

```