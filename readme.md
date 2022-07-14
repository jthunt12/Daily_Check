# Daily_Check -- SSL Certificate Audit

Daily_Check is a playbook that preforms a handshake with a list of URL's through specified ports. An email is then sent out to all recipients informing them of a certificates expiration date and how many days are remaining till expiration.

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

# Arguments

This playbook assumes that you are running from the following dir/ and assumes url_list.yml & mail_list.yml are in the vars/ folder.

```
/opt/ansible/daily_check/--> ../vars/url_list.yml
                             ../vars/mail_list.yml
```

** This part of the playbook can be modified by editing lines 12, 19, 34, 47, 61, & 66.

# Purpose

Once the playbook is ran either manually or through scripted processes, recipients will receive an email with the following outline.

![Capture](https://user-images.githubusercontent.com/36526335/179010910-d35da6a8-84ba-47ec-a81c-09c73e6320ac.JPG)