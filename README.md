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
and check it in browser port 5601
