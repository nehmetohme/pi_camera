# pi_camera

## Prepare Picam on a local repo or your own way!

* yum install httpd
* mkdir -p /var/www/html/repo/uk/co/caprica/picam/0.1.0-SNAPSHOT
* git clone https://github.com/nehmetohme/picam.git
* mvn clean install 
* cd picam
* cp ./target/picam-0.1.0-SNAPSHOT.jar /var/www/html/repo/uk/co/caprica/picam/0.1.0-SNAPSHOT/picam-0.1.0-SNAPSHOT.jar
* systemctl start httpd
* systemctl enable httpd


## pi-camera
* git clone https://github.com/nehmetohme/pi_camera.git
* Adapt the pom.xml to point to your local repo. eg. "<url>http://dexter:8788/repo/</url>"
* mvn clean install
* Deploy Bundle - ./target/pi-camera.0.1-SNAPSHOT.dp on Kura or Kapua!
