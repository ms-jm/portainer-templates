Certificates for XProtect can be created as described here:

https://doc.milestonesys.com/latest/en-US/portal/htm/chapter-page-certificates-guide.htm



How to create vms-authority certificate:

```bash
openssl x509 -inform der -in root-authority-public.cer -outform pem -out vms-authority.crt
```

How to create server certificate and private key:

```bash
openssl pkcs12 -in server.pfx -nocerts -out server.key -nodes
openssl pkcs12 -in server.pfx -clcerts -nokeys -out server.crt -nodes
```
