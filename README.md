Docker nodeBB
=====

nodebb-plugin-s3-uploads configuration
-----
Set your S3 parameters in your docker-compose yml file:
```
  environment:
   - AWS_ACCESS_KEY_ID=SET_THIS
   - AWS_SECRET_ACCESS_KEY=SET_THIS
   - S3_UPLOADS_BUCKET=SET_THIS
```
or in your run command like so:
```
        ...
        -e AWS_ACCESS_KEY_ID=SET_THIS \
        -e AWS_SECRET_ACCESS_KEY=SET_THIS \
        -e S3_UPLOADS_BUCKET=SET_THIS
        ...
```
