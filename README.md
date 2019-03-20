=> Data about the event that caused our virtual instance to die. Spot Instance related event can be detected through Spot Fleet API. We can run lambda function when such event occurs. However, EC2 and other virtual machine related event can be collected from AWS Cloud Watch service. Lambda can be invoked based on such EC2 disruption event.

=> Any virtual machine (EC2) context or event related information can be collected from AWS Cloud Watch monitoring system.

=> Spot Fleet API will be a crucial tool for our use case, as we target to minimize the server cost using Spot Instance ( most cheap virtual instance in AWS ) instead of using EC2 or any kind of other virtual machine deployments.
Spot Fleet offers various data related to disruption events, current price of Spot Instance for different specifications, Availability zones.


* Objective of the research is to use AWS Spot Instance to provide fault tolerant service to business or any critical scientific application in a minimal cost.

Amazon EC2 Spot Instances offer spare compute capacity available in the AWS cloud at steep discounts compared to On-Demand instances. Spot Instances enable you to optimize your costs on the AWS cloud and scale your application's throughput up to 10X for the same budget.

Using Spot Instance instead of EC2 instances at savings of up to 90% the On-Demand price.