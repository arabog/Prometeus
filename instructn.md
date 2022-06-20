Instructions:
Create a new EC2 instance. Micro/free tier works great!
If you don't have a key pair created already in your AWS Console, you should do that now. Folllow these instructions to create the key pair and save a copy to your computer in a file named keypair.pem.
SSH into the instance using the console using the key pair.
Install the application "Prometheus" using the instructions in this tutorial.

https://codewizardly.com/prometheus-on-aws-ec2-part1/

Open up port 9090 on the EC2 instance's security groups.
Browse to the Prometheus application using the EC2 instance's hostname and port 9090 to verify it's working.

