### A quick and dirty example on how to roll an AWS Lambda Function with serverless and dotnetcore on ubuntu

## Prerequisites

1) Serverless

```shell

npm -g install serverless
```

## Bootstrap template

```shell

sls create -t aws-csharp -p aws-lambda-csharp-example
dotnet migrate
rm -rf ./backup

```

## Build Function

```shell
dotnet restore
./build.sh
```

## Deploy

```shell
sls deploy
```

## Test

```shell
sls invoke -f hello
```
