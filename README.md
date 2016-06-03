# krb5client
Kerberos 5 Client

Implements a Kerberos client with authentication and administrative functionality.
Requires krb5 to be installed (please see http://web.mit.edu/kerberos/) and correctly
configured. Interaction with kerberos is done via the krb5 utilities
(kinit, klist, kdestroy, kadmin).

Kerberos 5 is supported by all? Linux platforms.

## Kerberos Installation
Arch linux: # pacman -S krb5

Cent OS: # yum install krb5-workstation

## Kerberos Configuration
The file /etc/krb5.conf must be edited to conform with your kerberos implementation.

A basic example is given below:
    [libdefaults]
        default_realm = COMPANY.COM
    [realms]
        COMPANY.COM = {
            kdc = kdc.company.com
            admin_server = kdc.company.com
            kpasswd_protocol = SET_CHANGE
        }
    [domain_realm]
        .company.com = COMPANY.COM
        company.com = COMPANY.COM
        


