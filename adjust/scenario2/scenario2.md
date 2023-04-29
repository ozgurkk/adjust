
Scenario 2
Question
Imagine a server with the following specs:
● 4 times Intel(R) Xeon(R) CPU E7-4830 v4 @ 2.00GHz
● 64GB of ram
● 2 TB HDD disk space
● 2 x 10Gbit/s nics

The server is used for SSL offloading and proxies around 25000 requests per
second. Please let us know which metrics are interesting to monitor in that specific
case and how would you do that? What are the challenges of monitoring this?

Answer
For the given system, there will be some crucial performance metrics to monitor. In summary, these are:  	 

1.	CPU usage per/sec: Important to know that our CPU’s utilization. If values are higher than 85% in long period, it means that the CPU is overloaded.
2.	Memory Free bytes/Kbytes or Megabytes: It is another vital info for us to know if there is enough amount of memory exist. If the memory utilization is higher than 85% of the actual memory, there will be performance issues. Also, 100% utilization causes critical server errors.
3.	Disk Queue Length: Tells us to amount of i/o request or requests that are waiting in the disk job queue. Shouldn’t be exceed 2. The values are higher than 2 means there is a disk congestion.
4.	Network Interface in/out/total Bytes: Shouldn’t be exceed the bandwidth of the NIC bandwidth. Otherwise, there will be a network congestion. 
5.	Latency: how long it takes for your service to process a request. 
6.	Rejected connections: Number of connections that were rejected by the server. Should be zero or an acceptable number of low values.
7.	Connection count: Knowing the number of connections that are currently active, allow us to see and know how serious our scenario.
8.	HTTP 5xx status codes: If this is a web server, need to monitor the number of server errors that occurred.

Challanges
The challenges of monitoring are:
1.	Accuracy: There will be huge amount of monitoring data, so it can be difficult to ensure that the data being collected is up-to-date.
2.	Data Storage: Based on the data collection frequency, storing and managing the monitoring data could be very challenging. In addition to that, it should be clear to know, what amount of period we should keep the monitoring data. It is strategic, if we keep for a short period like 1-2 months or fewer, we can’t predict or estimate for the future decisions, plans etc.

We can monitor these metrics via Prometheus with Grafana, New Relic, SolarWinds Server or similar. If our server is a cloud server, we can use the “CloudWatch” for AWS or “Azure Monitor/Sentinel” for Azure for logging and monitoring.

Each tool has its own advantages or disadvantages. Therefore, choosing agentless and lightweight tools would help us to accurate monitoring. Using an agent means that there will be an additional software run on the server. This means that agent consume from system resources, especially for a busy/overloaded server it can cause monitoring/logging inconsistencies.
	If using an agent-based solution is unavoidable, we should use a separate NIC and disk other than the server services use. By this way, monitoring traffic and agent disk i/o, monitoring cache wouldn’t be additional load to the server.


Comments

	The given system below is sized to meet for the high number of requests. The Intel E7-4830 v4 can be countable as outdated (first launched in Q2 of 2016, end of service expired in Jun, 2022).

Using mechanic disks (HDD) would raise disk based i/o performance problems. In the given scenario, using SSD’s or a storage array consisted of SSD disks with SAN or ideally “NVMe” based disk solutions would greatly eliminate disk I/O or latency problems. 

In addition to above, hopefully there are two 10G Nic’s placed in the server. If there is not an obstacle to use them together, and if it supports by driver/ or operating system, we can create a bond interface (sometimes it is called as multi-link etc.). Hence, the server network bandwidth would be greatly increased.

As I understand, there is just 1 server running, in the given scenario. Event SSL offloading done by a Load Balancer, increasing the server count in the pool would be greatly improve overall performance while increasing costs.





