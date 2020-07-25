# EFS
Using EFS and Attaching to EC2

#Important -> Use Same security group in Instance and EFS

sudo apt-get update<br/>
git clone https://github.com/aws/efs-utils<br/>
sudo apt-get -y install binutils<br/>
cd efs-utils/<br/>
./build-deb.sh<br/>
sudo apt-get -y install ./build/amazon-efs-utils*deb<br/>
sudo mkdir /mnt/efs<br/>
sudo mount -t efs fs-dfb6773d:/ /mnt/efs<br/>

#Optional Steps
cd /mnt/efs/<br/>
ls<br/>
df -h<br/>
history<br/>
sudo mkdir getting-started<br/>
sudo chown ec2-user getting-started<br/>
sudo chown ubuntu  getting-started<br/>
cd getting-started<br/>
touch test-file.txt<br/>
ls -al<br/>
