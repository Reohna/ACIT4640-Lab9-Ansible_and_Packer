# 4640-w9-lab-start-w25

See lab instructions on D2L


1. Generate SSH Keys
   ssh-keygen -t ed25519 -f ~/.ssh/<name_of_key>

2. Import Public key to AWS 
   sh ./script/import_lab_key ~/.ssh/<name_of_key>.pub

3. Built AMI #Run packer within packer directory, it is coded to have a relative path from packer/
   packer init packer/
   packer build .

4. Create the EC2 Instance
   cd terraform
   terraform init
   terraform validate
   terraform plan
   terraform apply
   terraform destroy

5. At the end of the terraform execution information, you should receive a dns name and an ip address. Use either one to go to the website:
   <img width="773" alt="labby" src="https://github.com/user-attachments/assets/72745d06-218c-42d0-a2a1-450fe3d04d8f" />


Troubleshooting

Unfortunately I do not have a default VPC, Subnet, and Public IP Address configured so I had to input those values within the file. Please replace the IDs with your own.
I know I should probably put it into the environment variables but I deleted them.
