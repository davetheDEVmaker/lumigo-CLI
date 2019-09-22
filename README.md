lumigo-cli
==========

A collection of helpful commands for working with AWS Lambda.

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/lumigo-cli.svg)](https://npmjs.org/package/lumigo-cli)
[![Downloads/week](https://img.shields.io/npm/dw/lumigo-cli.svg)](https://npmjs.org/package/lumigo-cli)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g lumigo-cli
$ lumigo-cli COMMAND
running command...
$ lumigo-cli (-v|--version|version)
lumigo-cli/0.4.0 darwin-x64 node-v10.16.0
$ lumigo-cli --help [COMMAND]
USAGE
  $ lumigo-cli COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`lumigo-cli analyze-lambda-cost`](#lumigo-cli-analyze-lambda-cost)
* [`lumigo-cli help [COMMAND]`](#lumigo-cli-help-command)
* [`lumigo-cli list-lambda`](#lumigo-cli-list-lambda)
* [`lumigo-cli replay-sqs-dlq`](#lumigo-cli-replay-sqs-dlq)
* [`lumigo-cli sls-remove`](#lumigo-cli-sls-remove)
* [`lumigo-cli tail-kinesis`](#lumigo-cli-tail-kinesis)
* [`lumigo-cli tail-sns`](#lumigo-cli-tail-sns)
* [`lumigo-cli tail-sqs`](#lumigo-cli-tail-sqs)

## `lumigo-cli analyze-lambda-cost`

Analyze Lambda functions costs in ALL regions

```
USAGE
  $ lumigo-cli analyze-lambda-cost

OPTIONS
  -p, --profile=profile  AWS CLI profile name
  -r, --region=region    only include functions in an AWS region, e.g. us-east-1
```

_See code: [src/commands/analyze-lambda-cost.js](https://github.com/lumigo-io/lumigo-cli/blob/v0.4.0/src/commands/analyze-lambda-cost.js)_

## `lumigo-cli help [COMMAND]`

display help for lumigo-cli

```
USAGE
  $ lumigo-cli help [COMMAND]

ARGUMENTS
  COMMAND  command to show help for

OPTIONS
  --all  see all commands in CLI
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v2.2.1/src/commands/help.ts)_

## `lumigo-cli list-lambda`

List Lambda functions in ALL regions

```
USAGE
  $ lumigo-cli list-lambda

OPTIONS
  -i, --inactive         only include functions that are inactive for 30 days
  -p, --profile=profile  AWS CLI profile name
  -r, --region=region    only include functions in an AWS region, e.g. us-east-1
```

_See code: [src/commands/list-lambda.js](https://github.com/lumigo-io/lumigo-cli/blob/v0.4.0/src/commands/list-lambda.js)_

## `lumigo-cli replay-sqs-dlq`

Replays the messages in a SQS DLQ back to the main queue

```
USAGE
  $ lumigo-cli replay-sqs-dlq

OPTIONS
  -c, --concurrency=concurrency    [default: 10] how many concurrent pollers to run
  -d, --dlqQueueName=dlqQueueName  (required) name of the SQS DLQ queue, e.g. task-queue-dlq-dev
  -n, --queueName=queueName        (required) name of the SQS queue, e.g. task-queue-dev
  -p, --profile=profile            AWS CLI profile name
  -r, --region=region              (required) AWS region, e.g. us-east-1
```

_See code: [src/commands/replay-sqs-dlq.js](https://github.com/lumigo-io/lumigo-cli/blob/v0.4.0/src/commands/replay-sqs-dlq.js)_

## `lumigo-cli sls-remove`

Deletes a CloudFormation stack that was generated by the Serverless framework

```
USAGE
  $ lumigo-cli sls-remove

OPTIONS
  -n, --stackName=stackName  (required) name of the CloudFormation stack, e.g. hello-world-dev
  -p, --profile=profile      AWS CLI profile name
  -r, --region=region        (required) AWS region, e.g. us-east-1
```

_See code: [src/commands/sls-remove.js](https://github.com/lumigo-io/lumigo-cli/blob/v0.4.0/src/commands/sls-remove.js)_

## `lumigo-cli tail-kinesis`

Tails the records going into a Kinesis stream

```
USAGE
  $ lumigo-cli tail-kinesis

OPTIONS
  -n, --streamName=streamName  (required) name of the Kinesis stream, e.g. event-stream-dev
  -p, --profile=profile        AWS CLI profile name
  -r, --region=region          (required) AWS region, e.g. us-east-1
```

_See code: [src/commands/tail-kinesis.js](https://github.com/lumigo-io/lumigo-cli/blob/v0.4.0/src/commands/tail-kinesis.js)_

## `lumigo-cli tail-sns`

Tails the messages going into a SNS topic

```
USAGE
  $ lumigo-cli tail-sns

OPTIONS
  -n, --topicName=topicName  (required) name of the SNS topic, e.g. task-topic-dev
  -p, --profile=profile      AWS CLI profile name
  -r, --region=region        (required) AWS region, e.g. us-east-1
```

_See code: [src/commands/tail-sns.js](https://github.com/lumigo-io/lumigo-cli/blob/v0.4.0/src/commands/tail-sns.js)_

## `lumigo-cli tail-sqs`

Tails the messages going into a SQS queue

```
USAGE
  $ lumigo-cli tail-sqs

OPTIONS
  -n, --queueName=queueName  (required) name of the SQS queue, e.g. task-queue-dev
  -p, --profile=profile      AWS CLI profile name
  -r, --region=region        (required) AWS region, e.g. us-east-1
```

_See code: [src/commands/tail-sqs.js](https://github.com/lumigo-io/lumigo-cli/blob/v0.4.0/src/commands/tail-sqs.js)_
<!-- commandsstop -->
