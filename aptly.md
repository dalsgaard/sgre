# Aptly Mirror

## Mirror Server

`apt install aptly`

`aptly mirror create -architectures=amd64 -filter-with-deps -filter='Name (ruby)' focal-demo http://dk.archive.ubuntu.com/ubuntu focal main`

`aptly mirror update focal-demo`

`aptly snapshot create focal-demo-1.0.0 from mirror focal-demo`

`aptly publish snapshot focal-demo-1.0.0`

`aptly publish snapshot -skip-signing focal-demo-1.0.0`

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
