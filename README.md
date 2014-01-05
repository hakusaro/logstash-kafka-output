# Logstash Kafka Output Plugin

This is a plugin for Logstash. The original author, [jeroenvandijk](https://github.com/jeroenvandijk/logstash) left a buggy implementation up that was incompatable with the newest version of the Kafka-rb gem. Because the associated input for Logstash is currently broken, it was not included either.

## Usage

1. Specify the plugin path during Logstash's statup: --pluginpath ./[where-you-cloned-the-repo-to]
3. ````rvm use jruby-1.7.8````
4. ````gem install kafka-rb````
2. Add the output to Logstash, implementing host, topic, and port information associated with Kafka.

````
output {
  kafka { host => 'localhost' topic => 'test' port => 9092 }
}
````
