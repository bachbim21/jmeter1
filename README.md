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
 - Arregate report: 
 - Latency: time request sent - time response start to received
 - Response time (Sample time, load time, elapsed time): time request sent - time response fully received ===> Response time = Latency + processing time