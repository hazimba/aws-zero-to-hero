## networking and virtual private cloud (VPC)

user stories - mockup understanding
example have village and lot of people, many type of people include lazy people, lazy people cant build their own house and looking for wise person (name is abc), abc want to take opportunity. abc buy some land in the village and ask requirement such what resources, size, want they want in return lazy people will give money. when 1 house is complete, other lazy people also want to have the services. all the construction, maintenance is done by abc. but they (all lazy people) realize that they houses build nearby to each other and concern about ##security breach. so abc dont want to lose business, abc purpose secure property (like access card) and this method for group. in group itself have is own security, when want to go specific house. also have specific instruction. this is solve security breach

let say region (MALAYSIA) - real situation

1. for example there are 3 compamy with 3 domain who cant afford datacenter and cant maintain it. so aws (wise person), building their own datacenter in malaysia (buy land). so aws can host their application in aws data center and company can make request on how many virtual machine and give aws money. so all 3 company will be serve in server 1. 1 of the company is startup and hacker manage to get into the company, so all in same server will get affected as hacker can access all data in the server. this issue back in 2013. so VPC is created to solve the issue that VPC is documented and manage by devOps

2. so given the project to devOps, devOps will make request to aws to create VPC and define the size of VPC by meaning is define IP address range. IP address range example is 172.160.0.01 (255x255) and will receive 65536. the project by devOps to handle can be only 1 TCS but inside it can be multiple sub project such payment, transport, transaction. for each of one sub project will be allocate inside the (land/ spaces) with specific IP address ranges meaning each sub project have their own IP address range name SUBNET. so each sub project can deploy one or more instances. all the subnet, and application inside the subnet can be only access through gateway. gateway is like a path to give direction to go to application inside the subnet. when first access gateway, the first access is public subnet. public subnet can be access through internet gateway, once user enter, there are load balancer have particular path called as router table that define how to should request go to application

user -> gateway -> public subnet -> load balancer (in aws called elastic load balance) -> router -> private subnet, SECURITY/ TARGET GROUP (AWS SECURITY) -> application

VPC have its own IP address such 172.16.8.0.1
while subnet inside VPC have /, such 172.16.8.0.1/24, 172.16.8.0.1/25, 172.16.8.0.1/26

## NAT GATEWAY - to study
