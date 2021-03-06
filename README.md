This is based on the official rabbitmq image with the following plugins enabled:
* rabbitmq_management
* rabbitmq_mqtt
* rabbitmq_shovel
* rabbitmq_shovel_management
* rabbitmq_web_stomp

## Tags

Each tag represents the version:
* latest is the latest stable build, 3.6.3
* 3.6.3 is the stable build
* 3.7.0m5 is 3.7.0 milestone 5 preview. Use this at your own risk.

The master branch is always the preview, i.e. 3.7.0m5 currently. Once that version is released then we should create that branch and configure docker to build that with the 3.7.0 and latest tags.

Master will then become the next milestone branch when thats ready.

## Notes on the milestone builds

Note: This is the current 3.7 branch which has not yet been released yet.

Current version: 3.7.0 milestone 4

If this build fails then we have to find the new version for the milestone as they remove it.

So in the Docker file we have two values, the version and milestone. For a stable release both should match but for a pre-release versions then they match the two parts of the download url
            
From https://github.com/rabbitmq/rabbitmq-server/releases find rabbitmq-server-generic-unix-*.tar.xz file, eg:

https://github.com/rabbitmq/rabbitmq-server/releases/download/rabbitmq_v3_7_0_milestone2/rabbitmq-server-generic-unix-3.7.500.2.tar.xz

Here version will be 3.7.500.2 and milestone 3.7.0_milestone2

