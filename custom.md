# Custom Repo

`# aptly repo create sgre-custom`

`# aptly repo add sgre-custom hello_1.0-1_amd64.deb`

`# aptly repo show sgre-custom`

`# aptly snapshot create sgre-custom-1.0.0 from repo sgre-custom`

`# aptly snapshot show sgre-custom-1.0.0`

`# aptly snapshot merge -latest sgre-combined-1.0.0 sgre-custom-1.0.0 focal-demo-all-1.0.0`

`# aptly snapshot show sgre-combined-1.0.0`

`# aptly snapshot filter -with-deps sgre-combined-1.0.0 hello-1.0.0 'Name (hello)'`

`# aptly snapshot show hello-1.0.0`

`# aptly publish snapshot -skip-signing hello-1.0.0`

`# aptly serve`
