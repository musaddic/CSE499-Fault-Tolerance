## A complete fault tolerance mechanism for scientific application using spot instance for cloud computing system.

##### Background Information, Issues  and Current Solutions

Most business use server with fixed computing resources such as Memory, Hard Disk, Processor etc. However, many businesses are shifting towards cloud where resources can be attached to the server on demand based which can deduct costs associated with unused resources. Although this on-demand rapid access to computing resources doesn’t require large upfront investments in hardware, most businesses who use this cloud computing services, do this process manually and inefficiently.

However, it is possible to build completely reliable, fault-tolerant and highly available system using modern cloud service providers like AWS. For example, AWS provides infrastructure building blocks which by themselves are fault-tolerant. But it is possible to achieve higher system availability and fault tolerance by using these infrastructures in such an arrangements and patterns so that any system failures such as massive DDOS attack, hard drives failures, power supplies failures, racks disruption etc. can be avoided very easily. In this research, I will propose a cloud infrastructure model which can use to achieve high availability and fault-tolerance for computing server and build the server model practically from scratch and test it with high traffic loads and stress script.


##### Importance of solving this problem

Achieve high availability and fault-tolerance in cloud computing with minimum expenditures and thus saving millions of dollar each year for hundreds of thousands businesses who are using computing server for various reasons.



##### The Main aims of this research

Just moving a web computing server into the cloud does not make it fault tolerant or highly available.  In this research, I’ll propose a cloud infrastructure model for in combinations with different availability zones, load balancers, elastic IP, server instances, auto scaling, cloud watch etc. to encourage business to achieve fault tolerant system for their business which will provide following benefits to the business:

1.	No failures of computing server, when the traffic or server usage is extremely high. Instead, system will auto scale itself based on usage of the resources and stress.

2.	Implementation of cloud watch to monitor computing load on system from the traffic.

3.	Auto snapshot mechanism to ensure correct backups and restoring.

4.	Auto computing instance creation from the snapshot when load/stress cross certain limit.
When traffic is low, cloud watch will send notification and unused instances will auto destroy themselves to reduce cloud service bills. 


##### The questions which need to be addressed in this research 

RQ1. Which kind of service / model is being used by the businesses currently.

RQ2.  What are the problems of current computing model used by most businesses?

RQ3. How can my cloud computing infrastructure model help businesses to avoid undesired system failures and save them from losing customers and money?

RQ3. How to build a complete fault tolerant and high available computing server at a very low cost?

RQ4. How I am going to suggest very powerful and unique cloud computing concept in combinations with cloud watch, auto-scaling, and load balancing.

RQ5. Compare the costs of my suggested fault tolerant system and other model using the same amount of traffic/load on the server.

RQ6. How can we make this model useful for all kind of businesses who uses computing for various purposes?

RQ7.  Study of various factors why business should switch to this model.

RQ8. Building a practical server based on this model in AWS and later test with load and stress.


#####	Current best solutions in cost aware Auto scaling mechanism

Zhang et al. (2016) , Kllapi et al. (2011) proposed an auto scaling schedule based framework
where optimized time and cost of independent cloud workflow execution is considered. According to Zhang’s scaling strategy, types of multiple cloud resources and cloud configuration combined of those resources are given high priority when designing the auto-scaling mechanism. Aslanpour el at. (2017) has proposed a solution for scaling of application equipping Suprex executor mechanism. This approach handles its operation following a MAPE concept with an strategy to save costs and limit exploitations of surplus resources. 


##### Limitation of current best solution

Although schedule based cloud workflow execution introduces unique optimization strategy for scaling supporting multiplication of EC2 based on the demand of load balancing and destroying them when needed, is not price efficient in occasion of new types of DDOS attack like Yo-Yo or very irregular traffic load pattern issues.

New kind of DDOS attack (Yo-Yo) or any irregular traffic pattern incur huge costs in current best solution. So, although this auto scale mechanism can make system fault tolerant it does not provide efficient cost-flow mechanism. 




##### Some of the researches on this area

References:

1.	R. Han, L. Guo, M. Ghanem, and Y. Guo, “Lightweight resource scaling for cloud applications,” in Cluster, Cloud and Grid Computing (CCGrid), 12th IEEE/ACM International Symposium on, 2012, pp. 644–651.

2.	Gandhi, A., Dube, P., Karve, A., Kochut, A., & Zhang, L. (2014, June). Adaptive, Model-driven Autoscaling for Cloud Applications. In ICAC (Vol. 14, pp. 57-64).

3.	Roy, N., Dubey, A., & Gokhale, A. (2011, July). Efficient autoscaling in the cloud using predictive models for workload forecasting. In Cloud Computing (CLOUD), 2011 IEEE International Conference on (pp. 500-507). IEEE.

4.	“Amazon auto scaling,” http://aws.amazon.com/autoscaling/

5.	Mao, M., Li, J., & Humphrey, M. (2010, October). Cloud auto-scaling with deadline and budget constraints. In Grid Computing (GRID), 2010 11th IEEE/ACM International Conference on (pp. 41-48). IEEE.

6.	“Azure AutoScale”,  https://azure.microsoft.com/en-us/features/autoscale/.

7.	“RightScale AutoScale”, http://docs.rightscale.com/faq/What_is_auto-scaling.html

8.	Zhang, Q., Cheng, L., & Boutaba, R. (2010). Cloud computing: state-of-the-art and research challenges. Journal of internet services and applications, 1(1), 7-18.

9.	Lorido-Botran, T., Miguel-Alonso, J., & Lozano, J. A. (2014). A review of auto-scaling techniques for elastic applications in cloud environments. Journal of Grid Computing, 12(4), 559-592.

10.	Kokkinos, P., Varvarigou, T. A., Kretsis, A., Soumplis, P., & Varvarigos, E. A. (2013, June). Cost and utilization optimization of amazon ec2 instances. In Cloud Computing (CLOUD), 2013 IEEE Sixth International Conference on (pp. 518-525). IEEE.

11.	H. Goudarzi, M. Ghasemazar, and M. Pedram, “Sla-based optimization of power and migration cost in cloud computing,” in Cluster, Cloud and Grid Computing (CCGrid), 2012 12th IEEE/ACM International Symposium on, 2012, pp. 172–179.

12.	Lorido-Botrán, T., Miguel-Alonso, J., & Lozano, J. A. (2012). Auto-scaling techniques for elastic applications in cloud environments. Department of Computer Architecture and Technology, University of Basque Country, Tech. Rep. EHU-KAT-IK-09-12.

13.	Rathnayake, S., Loghin, D., & Teo, Y. M. (2017, August). CELIA: Cost-time Performance of Elastic Applications on Cloud. In Parallel Processing (ICPP), 2017 46th International Conference on (pp. 342-351). IEEE.

14.	Yang, J., Liu, C., Shang, Y., Cheng, B., Mao, Z., Liu, C., ... & Chen, J. (2014). A cost-aware auto-scaling approach using the workload prediction in service clouds. Information Systems Frontiers, 16(1), 7-18.

15.	Fox, A., Griffith, R., Joseph, A., Katz, R., Konwinski, A., Lee, G., ... & Stoica, I. (2009). Above the clouds: A Berkeley view of cloud computing. Dept. Electrical Eng. and Comput. Sciences, University of California, Berkeley, Rep. UCB/EECS, 28(13), 2009.

16.	Varia, J. (2010). Architecting for the cloud: Best practices. Amazon Web Services, 1, 1-21.

17.	 Vaquero, L. M., Rodero-Merino, L., & Buyya, R. (2011). Dynamically scaling applications in the cloud. ACM SIGCOMM Computer Communication Review, 41(1), 45-52

18.	N. Roy, A. Dubey, and A. Gokhale, “Efficient autoscaling in the cloud using predictive models for workload forecasting,” in Cloud Computing (CLOUD), 2011 IEEE International Conference on. IEEE, 2011, pp. 500–507.

19.	Z. Gong, X. Gu, and J. Wilkes, “Press: Predictive elastic resource scaling for cloud systems,” in Network and Service Management (CNSM), 2010 International Conference on, 2010, pp. 9–16.

20.	Z. Shen, S. Subbiah, X. Gu, and J. Wilkes, “Cloudscale: elastic resource scaling for multi-tenant cloud systems,” in Proceedings of the 2nd ACM Symposium on Cloud Computing. ACM, 2011, p. 5.

21.	W. Iqbal, M. N. Dailey, D. Carrera, and P. Janecek, “Adaptive resource provisioning for read intensive multi-tier applications in the cloud,” Future Generation Computer Systems, vol. 27, no. 6, p. 871, 2011.

22.	Islam, S., Keung, J., Lee, K., Liu, A., 2012. Empirical prediction models for adaptive resource provisioning in the cloud. Future Gener. Comput. Syst. 28, 155–162

23.	Toosi, A.N., Qu, C., de Assunção, M.D., Buyya, R., 2017. Renewable-aware geographical load balancing of web applications for sustainable data centers. J. Netw. Comput. Appl

24.	Z. Li, H. Zhang, L. OBrien, S. Jiang, Y. Zhou, M. Kihl, R. Ranjan, Spot Pricing in the Cloud Ecosystem: A Comparative Investigation, Journal of Systems and Software, 114:1–19, 2016.

25.	 H. Kllapi, E. Sitaridi, M. M. Tsangaris, Y. Ioannidis, Schedule Optimization for Data Processing Flows on the Cloud, Proc. of SIGMOD International Conference on Management of Data, pages 289–300, 2011.

26.	Aslanpour, M. S., Ghobaei-Arani, M., & Toosi, A. N. (2017). Auto-scaling web applications in clouds: a cost-aware approach. Journal of Network and Computer Applications, 95, 26-4.
