# CloudTrail Bucket

I provide a bucket for cloudtrail and other resources.

## Paradigm Explained

1. CloudTrail writes to the bucket.
1. The bucket creates a SQS Queue job.
1. A worker reads the Queue and loads Elastic Search.
1. Afer a week the object expires.

## Command

`FILENAME=cloudformation.yaml STACKNAME=CloudTrailBucket deploy`
