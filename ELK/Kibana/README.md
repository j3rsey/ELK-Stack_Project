# Kibana

## 리소스

||CPU|MEM|Program|
|---|---|---|---|
|우분투|1|1|ElasticSearch, Kibana|
|우분투|1|1|Logstash|


## Installation

This is a normal paragraph:

    apt  update
    apt  install  -y  openjdk-8-jdk
    wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
    echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-7.x.list
    apt update
    apt install kibana
    
end code block.

## Exec

This is a normal paragraph:

   curl -XGET localhost:5601
   sudo service kibana start
   sudo service kibana status
   
end code block.
