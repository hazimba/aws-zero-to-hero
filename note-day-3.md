## day 3 13/5/2026

## EC2 instance - elastic cloud compute - ecc - ec2

- basically user requesting cpu, ram and disk from aws through virtual server
- example there are 1 computer but need to have many user can use it, so will create virtual server
- elastic - can be upscale and downscale

14:15 contoh soalan type of ec2 types - general, machine learning, data analytic and all depend on application

types ec2 instance - can be purchase

- general
- compute optimized
- memory
- storage
- accelerated

aws have multiple region accross the world, india, us, europe
why need to select to specific region?
need to make sure the data is close as possible
can select to other region but will take time for request, less latency (time taken for each request for the application and server to send response time)
for example maybank dont want their client info outside malaysia, so need to choose malaysia as region

availability zone - multiple datacenter in 1 region
.if anything happen cust still can access the application

## create an instance

public ip address IPv4

- can be access from anywhere
- use to login

note: followed the video that using ubuntu cause i have no idea
open terminal to downloaded file of key (/Desktop/aws/aws-login.pem)

--- RUN THIS TO OPEN UBUNTU TERMINAL THAT CONNECT TO AWS
ssh -i aws-login.pem ubuntu@32.236.12.194
and will return below

"The authenticity of host '32.236.12.194 (32.236.12.194)' can't be established.
ED25519 key fingerprint is SHA256:fSncjyzNqocuPj/LRjgTtSexI6AKDhw69qriOaQDYpI.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '32.236.12.194' (ED25519) to the list of known hosts.
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@ WARNING: UNPROTECTED PRIVATE KEY FILE! @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0644 for 'aws_login.pem' are too open. <------- NEED TO SOLVE THIS ISSUE, RUN BELOW
It is required that your private key files are NOT accessible by others.
This private key will be ignored.
Load key "aws_login.pem": bad permissions
aws@32.236.12.194: Permission denied (publickey,gssapi-keyex,gssapi-with-mic)."

ubuntu@ip-172-99-23-299:~$ sudo apt update ^C
Error: The update command takes no arguments
ubuntu@ip-172-99-23-299:~$ sudo su -
root@ip-172-99-23-299:~# apt update

deployed jenkins in aws

- security > inbound rules > create new rules (8080) - to access [public_IPv4_address]:8080
  to get the password: -
  ubuntu@ip-172-31-23-231:~$ sudo cat /var/lib/jenkins/secrets/initialAdminPassword
  2ce050d392504e32ad2734848c382680
