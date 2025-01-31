# Buzzline-03-dineshguru

This repository contains producer and consumer data containing the online order applciation. The data is produced using Kafka and consumer from Kafka topics into CSV files.


## File Descriptions

## 1.smoker_temps.csv

Purpose: This CSV file contains the base online order data, with timestamps and temperature readings at regular intervals.
Details:

The file includes columns for order id, order_id, customer_name,order_status,timestamp,	total_price	items,	shipping_method, delivery_statustimestamp and temperature.
The data is generated as part of the project to simulate online order readings over time.
    
 # Producer Script (csv_producer_dineshguru.py) Purpose: 
 This Python script generates messages based on the data in smoker_temp.csv and sends them to a Kafka topic. Details: Uses the smoker_temp.csv as input to generate and send messages with the online order and related custom fields to the Kafka topic. The script runs continuously, producing messages every 5 seconds (can be configured in the .env). Consumer Script (csv_consumer_dineshguru.py) Purpose: This Python script consumes the messages from the Kafka topic and writes them to a CSV file. Details: Reads messages from the Kafka topic and writes the data into output.csv. The consumer logs the process and writes additional information (like status_message, order_status, etc.) to the output file.   

 ## Setup and Usage
 Windows:
    .venv\Scripts\activate

Running the Producer To start the producer and begin sending messages to Kafka, run the following:
py -m producers.json_producer_dineshguru

Running the Consumer To start the producer and begin consume messages to Kafka, run the following:
py -m consumer.csv_consumer_dineshguru
