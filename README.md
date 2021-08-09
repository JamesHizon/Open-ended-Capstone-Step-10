# Open-ended Capstone Step 10

### Description
In this step, I am to design/develop a dashboard to monitor the resources (compute, storage, network, etc.) used in my deployment architecture.

I used AWS CloudWatch to display key metrics to analyze S3 metrics such as the amount of data stored for both buckets created.
Since the AWS EMR Cluster was unable to analyze metrics in desired manner, I simply took a screenshot of the Cluster running via "Monitoring" tab. Here, we can see key metrics for a given EMR Cluster without the need to create a dashboard. In addition, I desired to observe the Billing metrics, but that is also unavailable via the AWS Educate account.

### Details on Key AWS EMR Cluster
For AWS EMR, key metrics include HDFS utilization (percent of disk space being used currently), Total Load (number of concurrent data transfers), Memory available MB (memory available for allocation within clusters), Memory allocated MB (amount of memory allocated to cluster), and Capacity remaining GB (amount of remaining HDFS disk capacity). Once can also observe how many nodes are running at a given time, applications being submitted (i.e. Spark application).

The following is a link for more information about key CloudWatch metrics for Amazon EMR: https://docs.aws.amazon.com/emr/latest/ManagementGuide/UsingEMR_ViewingMetrics.html


### Deliverables
1. Real-time analytics AWS CloudWatch dashboard
2. Screenshot of one EMR Cluster that I used

