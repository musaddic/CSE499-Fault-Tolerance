Problem statement:

AWS or any cloud provider platform has the mechanism for solving fault tolerance or auto scaling approach based on the traffic/application load demand. However, Our target is not only to solve fault-tolerance problem, but to do it in a very minimal cost approach. 

Cloud computing providers actually needs to keep additional computing resources ready to provide when their customers demands. This on-demand scaling is the fundamental of cloud offering. However, these additional resources when not being used, just remains idle. So, they came up with a idea of offering these spare computing resources in a very cheap price but without any guarantee that long-term continuenity. They can just terminate these instances anytime they want ( based on their clients demand ) but will provide a warning before 2 minutes prior to termination. 

AWS named them Spot Instance. Most cloud users use them for one-time short computing events such as data analysis, scientific computing events where high computing ability is needed in cheaper price.

However, we have come up with the idea of using these Spot spared computing instances in business application and any backend service which actually needs to sustain for long-time and run without any disruption.
Cheap price and warning prior to 120 seconds of termination is our focal point. 

We have planned to design a mathematical algorithm ( plus practical system ) which can auto load balance and auto scale  up new instances utilising termination notice event and run without any disruption. 

Practical example: On a particular peak hour, our target application requires 15 virtual instances of specific configuration ( quad core processor, 8GB ram etc. ) to meet the traffic/computing demand. Now, if we use general computing virtual instances ( such as EC2 from Amazon ) it will cost us around 15 * 120 USD. But if we can use Spare Spot computing instances cost will be just around 15 * 8.7 USD. Huge savings but problem is we need to design this with fault tolerance and availability that can run without interruption. 

Dataset:

1) Current prices of the spare spot instances through Spot Instances

2) Instances termination event through Spot Fleet API.

3) Our current application load/ traffic usages from Cloudwatch monitoring system.

4) Hardware resources utilisation level ( like 67% cpu usage, 80% memory usage ) of any particular instance using Cloudwatch system.

5) Price prediction graph for Spot Instances