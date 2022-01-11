# Deploy Static Website on AWS

In this project, you will deploy a static website to AWS using S3, CloudFront, and IAM.

The files included are: 

index.html - The Index document for the website.
/img - The background image file for the website.
/vendor - Bootssrap CSS framework, Font, and JavaScript libraries needed for the website to function.
/css - CSS files for the website.


## Creating bucket

```bash
aws s3 mb s3://static-website-hwbz5a68
```

## Copying (syncing) content to bucket
```
aws s3 sync src s3://static-website-hwbz5a68
```

## Getting and setting bucket policy
```bash
# Setting
aws s3api put-bucket-policy --bucket static-website-hwbz5a68 --policy file://bucket-policy.json

# Getting
aws s3api get-bucket-policy --bucket static-website-hwbz5a68


```