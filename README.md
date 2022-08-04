# Music-Streaming-Cloud-Architecture-in-AWS-
Music-Streaming-Cloud-Architecture-in-AWS

Entertainment services are provided by a plethora of organizations all over the world. In the current scenario, a music organisation uses a traditional broadcasting system. Most of the activities are done manually - songs are recorded and stored physically in hard drives. On-premises servers are maintained with limited capacities. Songs are broadcasted as per the demands of customers. However, listeners cannot choose a particular song of their interest as they must rely on the request of ongoing public demand.  Hence, Walkman listeners store and carry the music of their choice in their pocket, but the library of music is too small. In addition, customer demand cannot be fulfilled sometimes because of the unavailability of a song in their limited server, and this situation affects the business plan of the organisation. The organisation needs resources to run the system effectively. There is a lack of scalability and flexibility in the system, and the maintenance cost of the resources are on the higher side. 

Therefore, a cloud-based infrastructure service is required to overcome these difficulties. Adoption of music streaming service in the organisation is looking for ways to expand their customer business, develop their products, cost variance, flexibility, scalability of IT infrastructure, profitability, and many more.  
 



**Illustration of System Architecture.**
Amazon route 53 distributes user requests (the traffic) to the infrastructure running (healthy endpoints) in AWS and manages the network traffic globally. The incoming application or network traffic are automatically distributed by Elastic load balancer to the available EC2 instances in single or multiple availability zones. EC2 instances support a variety of workloads of the application server in the auto-scaling group. The complete control of increased traffic load is performed by running scalable Amazon RDS on an EC2 instance. This is an example of an unmanaged service that can manage application optimization. Amazon RDS performs administrative tasks to reduce operational workloads and costs. Amazon elastic transcoder transcodes media files into a playable format and stores processed music files into an Amazon S3 bucket for distribution. Amazon CloudFront delivers requested song (music files) with low latency and high transfer speeds to the requested web page (output devices). Amazon CloudWatch alarm is used to trigger auto-scaling of EC2 instances when the latency of any one of the EC2 instances exceeds a preconfigured threshold.


![image](https://user-images.githubusercontent.com/80985027/167283219-186113f0-2bf8-476d-bb87-cc3d48ea74f4.png)
