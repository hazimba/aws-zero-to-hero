## day 2 13/5/2026

## accessibility

for example bank industry
where have many platform such debit, employee details or customer details (highly security and confidential)
so need to have authentication for authenticate to able to access those data
if dont have authentication, anyone can access

- as devop engineer

1. to create aws account
2. create policy for authentication to those services provided by aws such db related, kurbenates, ec2
3. root access using gmail - without policy/ IAM any user can make changes to configuration
4. so aws come out with IAM - authentication and authorization
5. so devop have their own gmail account not shared
6. from the root gmail account, can create user mail and give them access/ permission to specific service that they can acces
7. craete IAM - to solve the auth issue - example
   - users (aws users - authentication)
   - policies (attached some policies give them access to specific services)
   - groups (increase the efficiency, categorize)
   - roles

as root email (that signup and subscibe aws) can have all the policies, but it not recommended to configure the account using root email
instead, create a group such "devOp-engineers" and give all the policies and permission to handle the account, so that any
changes can be track instead 1 account is use by different people (devOp)

users is created via IAM page, when create user need to include

- username
- generated password that can be changed for first time login (also need to give access of "passwordchange")

group can also be created via IAM page

- can add more people of same group to have same permission/ auth/ policies

policies

- there a lot of policies handle by aws, but authd can create based on what they want
