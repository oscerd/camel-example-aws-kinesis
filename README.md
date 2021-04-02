# Camel AWS Kinesis example

### Introduction

An example which shows how to integrate Camel with a Kinesis stream.

You can configure your AWS account in the following file:
  `src/main/resources/kinesis.properties`

### Implementation


### Prerequisites

An AWS Account

### Build

You will need to compile this example first:

	mvn compile

### Run

To run the client you type:

	mvn compile exec:java 

Now run the following commands with the AWS CLI

        aws kinesis put-record --stream-name stream --partition-key 123 --data 'Kinesis message' --region <region>

You should see the following output
        {
            "ShardId": "shardId-000000000000", 
            "SequenceNumber": "49616945330772566342779944651221283872181791469110034434"
        }

and the message logged in the console.
