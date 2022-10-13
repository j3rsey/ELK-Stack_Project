# Logstash

## 리소스

||CPU|MEM|Program|
|---|---|---|---|
|우분투|2|4|ElasticSearch, Kibana|
|우분투|2|4|Logstash|


## Installation



    apt  update
    apt  install  -y  openjdk-8-jdk
    wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
    echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-7.x.list
    apt update
    apt install logstash
    

## Exec


    curl -XGET localhost:5000
    sudo service logstash start
    sudo service logsatsh status
