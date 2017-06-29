# AWS DynamoDB Local image

A Docker image containing a local development version of Amazon's DynamoDB, running in OpenJDK 9.

Several DynamoDB images already exist, like [this one](https://github.com/deangiberson/docker_aws_dynamodb_local) or [this one](https://github.com/vsouza/docker-dynamoDB-local), but I couldn't find one that had been updated with the [latest official build](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.html) of DynamoDB Local.

Sample usage (in [docker-compose.yml](https://docs.docker.com/compose/overview/)):

```
services:
  my_app:
    build: .
    depends_on:
      - dynamodb

  dynamodb:
    image: dabosq/dynamodb-local

```
