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

108  chmod 777 /var/run/docker.sock
  109  clear
  110  sysctl -w vm.max_map_count=524288
  111  clear
  112  sudo firewall-cmd --add-port=9200/tcp --permanent
  113  sudo firewall-cmd --add-port=5601/tcp --permanent
  114  sudo firewall-cmd --add-port=9600/tcp --permanent
  115  sudo firewall-cmd --add-port=9300/tcp --permanent
  116  sudo firewall-cmd --reload
  117  docker ps -a
  118  sudo apt-get update
  119  sudo apt-get install ufw
  120  sudo ufw allow 9200/tcp
  121  sudo ufw allow 5601/tcp
  122  sudo ufw allow 9600/tcp
  123  sudo ufw allow 9300/tcp
  124  sudo ufw enable
  125  clear
  126  curl -L -O https://artifacts.elastic.co/downloads/beats/metricbeat/metricbeat-7.16.3-linux-x86_64.tar.gz
  127  tar xzvf metricbeat-7.16.3-linux-x86_64.tar.gz
  128  cloud.id: "staging:dXMtZWFzdC0xLmF3cy5mb3VuZC5pbyRjZWM2ZjI2MWE3NGJmMjRjZTMzYmI4ODExYjg0Mjk0ZiRjNmMyY2E2ZDA0MjI0OWFmMGNjN2Q3YTllOTYyNTc0Mw=="
  129  cloud.auth: "metricbeat_setup:admin123"
  130  ./metricbeat modules list

and check it in browser port 5601
