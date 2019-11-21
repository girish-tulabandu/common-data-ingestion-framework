Connection of KAFKA with NIFI usecase
In this usecase, we are send logfile lines to apache kafka using the kafka producer from nifi, consume the files from kafka and store in the local 

TailFile processor fetch the log files

SplitTest processor splite the lines in the logfile as a flowfile

RouteOnContent processor it will search a word if it present it will send to the next processor

PublishKafka processor work as a kafka producer

ConsumeKafka processor get the flowfiles for every 10 secounds and put it in a single file and send to next processor to store
