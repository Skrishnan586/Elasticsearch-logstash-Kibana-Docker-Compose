# Elasticsearch-logstash-Kibana-Docker-Compose
Create ELK stack using Docker Compose
Create ELK stack using Docker Compose

 apt install docker.io -y
 sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
     sudo chmod +x /usr/local/bin/docker-compose
     clear
     docker-compose --version
     mkdir elk
     cd elk/
     mkdir logstash
     vi logstash.log
     paste the below data

     input {
  file {
    path => "/root/temp/inlog.log"
  }
}

output {
  elasticsearch {
    hosts => ["http://elasticsearch:9200"]
  }
}
save
mkdir temp in root cd to temp and create vi inlog.log wite some dummy text file and save

up the docker compose 

  chmod 777 /var/run/docker.sock
    clear
    sysctl -w vm.max_map_count=524288
    clear
    sudo firewall-cmd --add-port=9200/tcp --permanent
    sudo firewall-cmd --add-port=5601/tcp --permanent
    sudo firewall-cmd --add-port=9600/tcp --permanent
    sudo firewall-cmd --add-port=9300/tcp --permanent
    sudo firewall-cmd --reload
    docker ps -a
    sudo apt-get update
    sudo apt-get install ufw
    sudo ufw allow 9200/tcp
    sudo ufw allow 5601/tcp
    sudo ufw allow 9600/tcp
    sudo ufw allow 9300/tcp
    sudo ufw enable
    clear
    curl -L -O https://artifacts.elastic.co/downloads/beats/metricbeat/metricbeat-7.16.3-linux-x86_64.tar.gz
    tar xzvf metricbeat-7.16.3-linux-x86_64.tar.gz
    cloud.id: "staging:dXMtZWFzdC0xLmF3cy5mb3VuZC5pbyRjZWM2ZjI2MWE3NGJmMjRjZTMzYmI4ODExYjg0Mjk0ZiRjNmMyY2E2ZDA0MjI0OWFmMGNjN2Q3YTllOTYyNTc0Mw=="
    cloud.auth: "metricbeat_setup:admin123"
    ./metricbeat modules list

and check it in browser port 5601
