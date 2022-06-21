Instructions:
Create a new EC2 instance. Micro/free tier works great!
If you don't have a key pair created already in your AWS Console, you should do that now. Folllow these instructions to create the key pair and save a copy to your computer in a file named keypair.pem.
SSH into the instance using the console using the key pair.
Install the application "Prometheus" using the instructions in this tutorial.

https://codewizardly.com/prometheus-on-aws-ec2-part1/

Open up port 9090 on the EC2 instance's security groups.
Browse to the Prometheus application using the EC2 instance's hostname and port 9090 to verify it's working.

To download prometheus:
wget https://github.com/prometheus/prometheus/releases/download/v2.19.0/prometheus-2.19.0.linux-amd64.tar.gz


To exstract d dwloaded file: 
tar xvfz prometheus-2.19.0.linux-amd64.tar.gz

cd into the folder:
prometheus-2.19.0.linux-amd64

check version:
prometheus --version

cat prometheus.yml 

start prometheus in terminal:
./prometheus --config.file=./prometheus.yml

check prometheus in browser using the public dns with ur port:
ec2-107-20-73-211.compute-1.amazonaws.com:9090

to modify the prometheus.yml file:
nano prometheus.yml


To remove:
sudo cp prometheus-2.19.0.linux-amd64/prometheus /usr/local/bin
sudo cp prometheus-2.19.0.linux-amd64/promtool /usr/local/bin/
sudo cp -r prometheus-2.19.0.linux-amd64/consoles /etc/prometheus
sudo cp -r prometheus-2.19.0.linux-amd64/console_libraries /etc/prometheus

sudo cp prometheus-2.19.0.linux-amd64/promtool /usr/local/bin/

rm -rf prometheus-2.19.0.linux-amd64.tar.gz prometheus-2.19.0.linux-amd64

