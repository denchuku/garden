---
aliases: ["Google Cloud"]
---
Install Google Cloud SDK (includes `gsutil`):
```shell
brew install google-cloud-sdk
```

Copy 
```
gsutil -m cp -r ./localdir/** gs://bucket.domain.name/remotedir-tmp

gsutil rm -r gs://bucket.domain.name/remotedir

gsutil mv gs://bucket.domain.name/remotedir-tmp gs://bucket.domain.name/remotedir
```