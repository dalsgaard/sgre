# Aptly Mirror

## Mirror Server

`# apt install aptly`

`# aptly mirror create -architectures=amd64 -filter-with-deps -filter='Name (ruby)' focal-demo http://dk.archive.ubuntu.com/ubuntu focal main`

`# aptly mirror update focal-demo`

`# aptly snapshot create focal-demo-1.0.0 from mirror focal-demo`

`# aptly publish snapshot -skip-signing focal-demo-1.0.0`

`# aptly serve`

## Target Server

`# nano /etc/apt/sources.list`

In _sources.list_
`# deb [trusted=yes] http://172.17.0.2:8080/ focal main`

`# apt update`

Should fail
`# apt install python`

Should success
`# apt install ruby`

`# ruby -v`

## Updating Snapshot

`aptly mirror create -architectures=amd64 -filter-with-deps -filter='Name (python3)' focal-demo-ext http://dk.archive.ubuntu.com/ubuntu focal main`

`# aptly mirror update focal-demo-ext`

`# aptly snapshot create focal-demo-ext-1.0.0 from mirror focal-demo-ext`

`# aptly snapshot merge -latest focal-demo-all-1.0.0 focal-demo-1.0.0 focal-demo-ext-1.0.0`

`# aptly publish switch -skip-signing focal focal-demo-all-1.0.0`

`# aptly serve`

## Updating Target

`# apt update`

Should success
`# apt install python3`

Should fail
`# apt install python2`

## Misc

`cat /root/.aptly/public/dists/focal/main/binary-amd64/Packages`
