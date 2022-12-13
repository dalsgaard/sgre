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

```
-----BEGIN PGP PUBLIC KEY BLOCK-----

mQENBGOYjNABCADjpG9VrLe5nmtL/kkiOOY8683e+ugqFsVR+aY65+RnIP01v3KJ
YKdlR3Qdt/shtmpB7td3+OcpYEGdxkCLePhLbYFVUtoRYqxvNDEthM9wPbDJREWb
usp9MmL9oI1nAH6q6AoEdo5lKoyLwIKAaaWVOTkPhlEt3NNWfM1AwrG8XGKW8Cti
wAdpEtNzXv93sbSgGmwIUM+EqA1ECWOLxaaOtomSJ6mjGLGjN8+BhHww45hPV6G4
n3eXUp70AqRkMshoxNnAiFSlq8qxF7iHS7PC3aE3YaR63fin+bBk7qjk6JlQB65Y
AHm9R/M275uPNECut2BXgH9i8qoxHQGqBlATABEBAAG0JEtpbSBEYWxzZ2FhcmQg
PGtpbUBraW1kYWxzZ2FhcmQuY29tPokBOAQTAQgAIgUCY5iM0AIbAwYLCQgHAwIG
FQgCCQoLBBYCAwECHgECF4AACgkQe1rdSRaU4OmkHwf/ajkwxiu2vPfNYvNoWcvY
yP6NRu2iOogIIKNVlIbkvXcyHLcaSC7Pt+CfUBLpOWRuoLkKmk09P/lX0jhzJZBD
5K8Xak41NDQC7CfCZBz46UrMYfS0NhR9EhCqPLlu2UTsV0+jJa9QetE/t0qzntbC
52ttU9IUs2Z6ebSU8UvzmAOZ5u4PBPUPeFcvfnD8Y9aij/rtKxhTXxL7QFaoQZnM
eGQXB5svPDndnQ498dh+quSxj+i/jSP+PI5DqfJySbWloxPth5qZqaJLb7rKFzQG
9C9sJPXVrN4AfGPXxOxhGognUf2++9Mu/BD6GxG+RLGdAe7guFkbazo3mhA50Wqe
BLkBDQRjmIzQAQgA12lJSG3S5/ya+aMiK9EcpXLdlPCgRRyMN6vpHccmX+emlvsu
xA9us8p7p5fhEed8XupDKRZVspp4F4HIO7/KzlqKZL/ioJhLjGJf+e0JjKW3m2mY
xcyaoaxbp5WmlFexsVKm3y8sdDcQsrMA6T32TIXx1uNeHY+LAaMh++fQTk+jEK7e
G4HoED64LJiKf03kUeL2SXS9RMSUC9C9z5/ipl7u0Slt5PBjhwlufSsnXwJ/LI8q
lHtwaRHpO2xAEewOAcwS9N71Hc5Wulg7P1WS/SqXarZFZVzoap5dQB1k82PYOkdZ
fVYbiQGYbBCirGLi43pZT/Kq0F8Pa1I7ItmdmwARAQABiQEfBBgBCAAJBQJjmIzQ
AhsMAAoJEHta3UkWlODpj4cIAKTY3KFRLtA1VWhqxvHUH/n3cZaIaw+Yn4pQ7MYU
N3jIoXKGhVFg3vIrPuCvAwDYDjnhfDVrySZMcZpFIUsmzUxZG4I6R7CKcCfHmVmX
bbSM5drSeFoWv5hwl9Tg3DMldii7vwnnf2yOcwW6MlVkrvLmBygdnaZev6Mj3aR6
r0whbXj0+oZVqFhvdl4+kMQDPQcnvN3RNmhCkYc+O1KFdBrXgDPHCx1gpaltRIac
0aykLwv9e3IcV3QVG2ylwQd3qFvZBby6AscFy2C5P+DTQWbtF1RatjPfuT6X6+hm
ffWgL6oJ+4GrRsfIbsS84CcYxpzlzLxTn6yUTSRPkJDFpa4=
=Z4mX
-----END PGP PUBLIC KEY BLOCK-----
```
