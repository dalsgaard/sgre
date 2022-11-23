# dpkg

`# mkdir -p hello_1.0-1_amd64/DEBIAN`

`# touch hello_1.0-1_amd64/DEBIAN/control`

```
Package: hello
Version: 1.0
Depends: ruby (>= 2.0.0)
Architecture: amd64
Maintainer: Kim Dalsgaard <kim@kimdalsgaard.com>
Description: A text file with a greeting
 You can add a longer description here. Mind the space at the beginning of this paragraph.
```

`# mkdir -p hello_1.0-1_amd64/opt/hello`

`# touch hello_1.0-1_amd64/opt/hello/hellooo.txt`

```
Hellooo World!
```

`# dpkg-deb --build --root-owner-group hello_1.0-1_amd64`

`# dpkg -i hello_1.0-1_amd64.deb`

`# cat /opt/hello/hellooo.txt`

`#dpkg -r hello`

`# cat /opt/hello/hellooo.txt`
