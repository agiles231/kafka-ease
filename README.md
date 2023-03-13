# Kafka Ease
Kafka Ease provides scripts that improve user experience by avoiding duplicate boilerplate arguments.
Additionally, some scripts simplify common operational processes, or report data in a desired format.

* `rebalance-partitions`: Rebalance partitions
* `verify-rebalance`: Verify that rebalance is successful. Will use the file generated from `rebalance-partitions` to identify the rebalance, therefore you cannot run another rebalance if you wish to use this to verify
* `create-topic <topic_name> <partitions> [OPTIONS]`: Create a topic. OPTIONS are passed to `kafka-topics.sh` script that comes with kafka.
* `list-topics [OPTIONS]`: List all topics. OPTIONS are passed to `kafka-topics.sh` script that comes with kafka.
* `describe-topic <topic_name> [OPTIONS]`: Describe a topic. OPTIONS are passed to `kafka-topics.sh` script that comes with kafka.
* `describe-all-topics [OPTIONS]`: Describe all topics. OPTIONS are passed to `kafka-topics.sh` script that comes with kafka.
* `get-all-topic-partition-count`: List partition counts for all topics

Additionally, two scripts are helper scripts:
* `connect-zookeeper`
* `kafka-cmd`

`config` contains environment variables that need to be configured before using this tool.

## To deploy
* You can drop these scripts anywhere. By default, they are assumed to be in the kafka installation. If not, you will need to change `kafka_home` variable in `config`
* Change `bootstrap_server_url` in `config` to point to your bootstrap servers
* Change `zookeeper_url` in `config` to point to your zookeeper server

## To use
1. Configure by setting variables in `config`
2. Run desired script
