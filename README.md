# CMPE-281---Cloud-Technologies


Playing with Amazon’s EC2						- Shreekar Kolanu(017406493)

Assignment – 1

Step -1 : Login to AWS with IAM user always.

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/d7cb87b8-00e7-403b-88e5-02a8180af990)

 
![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/a22800df-6ae3-461e-9d00-9a474f8163e7)

 
Logged in to the AWS account
From the Dashboard visit EC2

Step – 2: We should launch an EC2 Instance

 ![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/96ee1cc5-4ade-4aec-ba93-2fde5efbb8e7)


I have named my ec2 instance as CMPE 281 and selected Ubuntu as my AMI image.

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/7b3e0caf-34a4-470c-b5d3-c09d535666ad)
 



I have selected my instance as t2micro (free tier) and have created a key pair already named demo281.

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/e260b764-c8af-4c3b-83c4-910daa3304d7)
 

I have configured a new security group and enabled all traffic but limited to my IP address.

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/764becbb-7981-4162-a0bf-b6738673360e)

 
Add the Jenkins script to run on the Ubuntu server

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/71749625-de3e-482d-8a91-25459b69de96)
 


Now the instance is ready and running

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/e9da2cd1-142a-42a2-acfa-f32f07cbfe6c)
 



Now we are accessing the ubuntu ec2 instance via cmd with the key pair 

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/32efe8be-f3d9-456b-ae59-e5261a2aae80)

 

Now we have accessed the ubutu ec2 instance

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/98238496-4728-4dea-936c-2721c593f52d)
 


Exposing the default port on 8080 to run Jenkins on our instance

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/067cbeb3-9a73-4072-a2f0-e0198d4475af)

 

We now enable Jenkins, start the service and fetch the status.
 
![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/b6e93340-ae2e-4d0f-9306-37e1c07b4d82)



We now open the public ip address

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/1d69e200-3cd3-40ce-8c4f-982e64539824)
 


Now we access the ip address with port 8080  

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/21a56af0-53f3-4587-a546-76c7c6b5235b)

Jenkins is exposed to 8080 port. http://44.203.155.182:8080

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/d6d92aeb-b159-4fcd-b663-fd6929130f7a)
 

Now we add cloudwatch metrics – Network out, Network In and CPU utilization to observe and monitor our instance.

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/0cfd4973-e318-4a16-bc47-8667bead3485)
 

As of now we don’t see and cpu utilization

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/22030fd3-6960-4a55-a1fb-5673a1120926)
 



We have downloaded the pem key in the location and used the path in the directory and connected to our instance via ssh/

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/1e3fd82d-bcf4-4287-ae72-e912e464af12)
 


Now we increase the load on the server by installing the package stress.

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/58d0b0b3-8ae0-4ae8-96ff-a976d09f3cd7)

 
Now we monitor the logs on cloud watch and check the CPU utilization as we can see it has increased to 17%

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/5f2554ff-0bb9-444f-8013-6b3a694ada46)
 


Now we can see that the CPU utilization to less that 1%

![image](https://github.com/Skillz619/CMPE-281---Cloud-Technologies/assets/43133388/b9f05d4b-abcd-44f7-90dc-1b0f21160382)
 
