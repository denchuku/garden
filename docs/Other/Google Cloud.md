Install Google Cloud SDK (includes `gsutil`):

````shell
brew install google-cloud-sdk
````

Copy content (including all files and sub-directories) of local directory `localdir` to bucket directory `remotedir-tmp`:

````shell
gsutil -m cp -r ./localdir/** gs://bucket.domain.name/remotedir-tmp/
````

The trailing `/` is important.

Remove and Move

````shell
gsutil rm -r gs://bucket.domain.name/remotedir

gsutil mv gs://bucket.domain.name/remotedir-tmp gs://bucket.domain.name/remotedir
````
