# auto-youtoube-stream-archiver
Github workflow to automatically download youtube livestreams and upload them to archive.org

## Setup For Your Own Stream

1. Fork this repository
2. Set the GitHub repository secrets `ACCESS_KEY` and `SECRET` to your archive.org account (create one if needed) S3 access key and secret key which can be found at https://archive.org/account/s3.php.
3. In the `.github/workflows/streamarchiver.yaml` file, Set the `bucketname` environment variable in the `upload` step to your desired bucketname and the `channelid` variable in the `download` step to your Youtube channel id.
4. If desired, modify the `curl` request in the `upload` step (to include metadata for example). See archive.org [developer docs](https://archive.org/developers/ias3.html) for more details.
