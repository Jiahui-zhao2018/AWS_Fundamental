# Getting Started with AWS Cloud

## What is the Cloud?
Cloud computing is the on-demand delivery of IT resources over the internet with pay-as-you-go pricing. Companies like AWS own and mantain these data centers and provide virtualized data center technologies and services to users over the internet. 
* If you run your application on-premises, creating and changing environment requires you to buy and install hardware, connecting cabling, and more.
* If you run your application in the cloud, you can replicate the entire environment as often as needed.

In summary, there are six benefits of Cloud Computing
1. __Pay as you go.__
1. __Benefit from massive economies of scale.__ By using cloud computing, you can achieve a lower cost than you can get on your own.
1. __Stop guessing capacity.__ You can access as much or as little capacity as you need, and scale up and down as required with only a few minute notice.
1. __Increase speed and agility.__ You can reduce the time to make those resources available to your developers from weeks to minutes.
1. __Stop spending money running and mantaining data centers.__ 
1. __Go global minutes.__ 


## AWS Global Infrastructure
In AWS, the physical infrastructure that makes up the AWS Global Infrastructure is in the form of Availability Zones and Regions. 

![Region](./assets/figures/Getting_started/region.svg)

__Regions__ are geographic locations worldwide where AWS hosts its data centers. When deciding which AWS Region to host your applications and workloads, you should consider four main aspects:  
1. __Latency.__
1. __Price.__
1. __Service availability.__
1. __Data compliance.__

Inside every Region is a cluster of __Availability Zones__. An AZ consists of one or more data centers with redundant power, networking, and connectivity.　　

Depending on the AWS Service you use, your resources are either deployed at the AZ, Region, or Global level. Each service is different, when you operate a Region-scoped service, you only need to select the Region you want to use, and AWS automatically performs actions to increase data duability and availability. On the other hand, some services ask you to specify an AZ, and you are often responsible for increasing the data durability and high availability of these resources.  
To keep your application available, you need to mantain high availability and resiliency. A well-known best practice for cloud architecture is to use Region-scoped, managed services which come with availablility and resiliency built in. When that is not possible, make sure the workload is replicated across multiple AZs.

## Interacting with AWS
Every action you make in AWS is an API call that is authenticated and authorized. In AWS, you can make API calls to services and resources through the AWS Management Console, the AWS Command Line Interface, or the Software Development Kits(SDKs).