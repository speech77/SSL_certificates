# create a root authority cert
```shell
./create_root_cert_and_key.sh
```

# create a wildcard cert for `mysite.com`
```shell
./create_certificate_for_domain.sh mysite.com
```

# create a cert for `www.mysite.com`, no wildcards
```shell
./create_certificate_for_domain.sh www.mysite.com www.mysite.com
```

# add root CA certificate
## Ubuntu
```shell
certutil -d sql:$HOME/.pki/nssdb -A -n 'mysite.com CA' -i rootCA.pem -t TCP,TCP,TCP
```
