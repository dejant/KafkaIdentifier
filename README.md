# KafkaIdentifier
Willkommen zu unserem Repo, mit welchem du mittels deiner Kamera Menschen erkennen kannst. Das Videos wird dabei über Apache Kafka gestreamt.

# Installationsanleitung
Kafka-Download:
https://downloads.apache.org/kafka/2.6.0/kafka_2.13-2.6.0.tgz

Benötigte Dependencies:
kafka-python  
opencv-python  
Flask  
numpy  
picamera  
Pillow  

Wechsel ins entsprechende Laufwerk, wo Kafka installiert wurde. Eröffne dabei für jeden Punkt einen eigenen Terminal.

1. Start Zookeeper:
bin/zookeeper-server-start.sh config/zookeeper.properties

2. Start Server:
bin/kafka-server-start.sh config/server.properties

3. Start Consumer:
python3 consumer.py

Nun sollte im Terminal folgendes erscheinen
Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)

4. Start Producer:
python3 producer.py
Der Videostream läuft nun.
Gehe in deinen Browser und öffne den folgenden Link:
http://0.0.0.0:5000/video 
Der Videostream sollte erscheinen.
