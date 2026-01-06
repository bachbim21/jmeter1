# jmeter1
Start learning

YTB source: https://www.youtube.com/watch?v=inNLWfqFRqM&list=PLlc3Nq1yAXsbqdD__OGcraEMPKKZkrd8-&index=15

## GraphQL 
 - Must be transfered into Json format then running later
 - Link:  https://www.postman.com/devrel/graphql-examples

## Assertion

 - optimize view result tree
 - add assertion

## Thread group 

Properties
 - Number of threads (user): number of simulate user
 - Ramp - up: time for each user to execute (Ex: user = 10, ramp-up = 60 ==> 6s for each user ===> 0s: user1, 6s: user2, 12s: user 3)
 - Loop count: user still run Sampler http request for number of count loop
 - Same user on each iteration: for purpose save pc's resource
 - Delay thread creation until needed: for purpose save pc's resource
 - Duration: time for entire thread
 - Start up delay: delay before excute thread
 
## Listener

 - View result in tree: show result by table
 - Response time graph: Display on graph
 - Arregate report: ***** (Percentile in Performance Testing)
 - Simple data: Modify file report
 - Latency: time request sent - time response start to received
 - Response time (Sample time, load time, elapsed time): time request sent - time response fully received ===> Response time = Latency + processing time
 
## Percentile in Performance Testing

In performance testing, percentiles are used to analyze and report how a system performs for a certain percentage of users or requests, especially when looking at response times (latency) or throughput. They help identify how most users experience the system’s performance, and they can show outliers or anomalies in the data.
 - 50th Percentile (P50): Also known as the median, it indicates the response time below which 50% of the requests are served. It represents the “typical” performance experienced by users.

 - 90th Percentile (P90): It indicates that 90% of the requests were completed within this time, meaning the response time for 90% of users is better than or equal to this value, and the slowest 10% of requests took longer than this.

 - 95th Percentile (P95): It tells you that 95% of the requests are completed within this time. This is a commonly used metric for performance SLAs (Service Level Agreements) since it excludes the extreme outliers (5% of the slowest responses).

 - 99th Percentile (P99): This is the response time below which 99% of the requests are served. It captures the worst-case performance for nearly all users, highlighting rare but critical slowdowns.
 
## Timer

Mimic scenario like real client
 - Constant timer: delay between each request
 - Uniform random timer: (followed formula: random(0.0 ~ 0.9) x random delay max + constant delay offset) mimic client action, ex: request1 is quick, but then client need more time to do request2

## Loop Controller and If Controller

 - Loop controller: Loop x times for each user
 - If controller: Run if condition meet (Using JSR223 for logic check)

## Simple controller and Module controller, Test fragment, include controller

 - Simple controller: Group single request into a group ---> Highly recommend
 - Module controller: Option to run simple controller (even simple controller is disable). Should be set up in "module to run", only apply for logic controller
 - Test fragment: auto disable
 - Include controller: Run request indicated by user (before: user save a request with: save as test fragment)
 - Random Controller: random "n" request in range || Random order controller: random all request in range