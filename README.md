Docker nodeBB
=====
Easy start
-----
I have included a docker-compose.yml file for your pleasure. Outside of setting the redis volumes portion (and replacing the S3 parameters, *see below*, if you want to run nodebb-plugin) you should be able to start your nodebb up and Compose will run your application.

nodebb-plugin-s3-uploads configuration.
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

TODO
----
* Figure out if there is an advantage to run Jessie on the redis container as well