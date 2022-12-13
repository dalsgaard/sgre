# Signing


### Install the correct version of GPG
```
apt install gnupg1
```

### Generate a key pair
```
gpg1 --gen-key
```

### Export the public key
```
gpg1 --export --armor kim@kimdalsgaard.com > kim-pubkey.asc
```

### Copy the key ring to the current directory
```
cp /root/.gnupg/pubring.gpg .
```

### Publish a signed snapshot
```
aptly publish snapshot --keyring=./pubring.gpg sgre-combined-1.0.0
```
