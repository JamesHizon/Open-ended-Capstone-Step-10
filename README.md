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

### Link to AWS CloudWatch Dashboard
Link: https://cloudwatch.amazonaws.com/dashboard.html?dashboard=Capstone_Dashboard&context=eyJSIjoidXMtZWFzdC0xIiwiRCI6ImN3LWRiLTcwNDQwOTE4MjcyOCIsIlUiOiJ1cy1lYXN0LTFfSHl0VG05cW5mIiwiQyI6IjFoMHR1YmFzZGltMTlnaGtmbms3MWFwMWttIiwiSSI6InVzLWVhc3QtMToyYWFmOGRmMS04ODA4LTRhMzYtODRlNS05ODA2ZjdjYmNhYjciLCJNIjoiUHVibGljIn0=

As you study these two metrics in real-time, you can see that the available EMR YARN MemoryAvailable is down to nearly 83% and that the oecbucket has no data available. Why is this? I ended up calling a method inside my EMR Notebook that would remove all files to see if that is possible. I was still able to work perform ELT work using nearly 100 GBs of data. It is also key to understand that it may take some time for the dashboard to obtain data related to S3 bucket size, but it still is near real-time.
