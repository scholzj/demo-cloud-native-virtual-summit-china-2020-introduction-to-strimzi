# Cloud Native + Open Source Virtual Summit China 2020: Introduction to Strimzi

* Create namespace Kafka
  * `kubectl create namespace kafka`
  * `kubectl config set-context --current --namespace=kafka`
* Install the Strimzi operator
  * `kubectl apply -f 'https://strimzi.io/install/latest?namespace=kafka'`
  * Explain what it installs
  * Mention other installation methods: Helm Charts, Operator Hub
* Show the simple Kafka CR
  * `bat 01-simple-kafka.yaml`
* Show the more complex Kafka CR
  * `bat 02-better-kafka.yaml`
  * Deploy it: `kubectl apply -f 02-better-kafka.yaml`
* Show how it deploys and explain the steps
  * Zookeeper first
  * Kafka next
  * Topic and User Operator
  * Kafka Exporter
* Show and deply the user
  * `bat 03-user.yaml`
  * Deploy it: `kubectl apply -f 03-user.yaml`
* Show and deply the topic
  * `bat 04-topic.yaml`
  * Deploy it: `kubectl apply -f 04-topic.yaml`
* Show and deply the Hello World app
  * `bat 05-hello-world.yaml`
  * Deploy it: `kubectl apply -f 05-hello-world.yaml`
  * Show how it consumes the messages