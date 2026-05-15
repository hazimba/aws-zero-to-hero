15/5/2026

## VPC is most important service in AWS

because vpc is introduce the concept private cloud in the world
without vpc, security and aws is no good

to learn in day 5: Theory + Practical

- security group +
  as devops > created vpc > define size of vpc > divide subnet > then within vpc have multiple private projects that cant be access to internet (subnet) and also internal project > so when user from internet want to access > go to internet gateway > devops will place load balancer > load balencer that have access to private subnet > and user have access to load balancer > load balancer can do configuration such restrict traffic etc > once load balancer forward the request to private subnet > the layer of subnet can add more security in subnet level > in layer can add security of ec2 > in subnet (inside the layer) can add security using NACL > meaning in AWS there are multiple way to add security > organization will put the application inside the public vpc > data will inside private vpc

## security in AWS is shared responsibility

can add security in by devops

1. security group
2. vpc
3. api gateway
4. subnet - NACL
