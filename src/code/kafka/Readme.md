# Integrating Kafka with NiFi
In this usecase, we are sending logfile lines to apache kafka using the kafka producer and storing in the local 

TailFile processor is used to  fetch the log files

SplitTest processor split the lines in the logfile as a flowfile

RouteOnContent processor will search a word if it present, if yes, it will send to the next processor

PublishKafka processor works as a kafka producer

ConsumeKafka processor get the flowfiles for every 10 secounds and put it in a single file and send to next processor to store
