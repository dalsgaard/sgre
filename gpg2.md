# Signing


### Install the correct version of GPG
```
apt install gnupg2
```

### Generate a key pair
```
gpg --full-generate-key
```

### List private keys
```
gpg --list-secret-keys
```
#### Output
```
/root/.gnupg/pubring.kbx
------------------------
pub   rsa3072 2022-12-14 [SC]
      84D1C9ECE301CBBD482AEEA310E2FACE364C9344
uid           [ultimate] Kim Dalsgaard <kim@kimdalsgaard.com>
sub   rsa3072 2022-12-14 [E]

```

### Export the public key
```
gpg --output kim-public.asc --armor --export 10E2FACE364C9344
```

### Export the private key
```
gpg --output kim-private.asc --armor --export-secret-key 10E2FACE364C9344
```

### Import the private key
```
gpg --import kim-private.asc
```

### Publish snapshot
```
aptly publish snapshot --gpg-provider=gpg2 sgre-combined-1.0.0
```
