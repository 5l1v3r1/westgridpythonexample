# West Grid Python Example

This script is used to show how to go about running a python batch job on the West Grid clusters.

## Requirements

In order to run the script on West Grid you must have access to West Grid, and that is the only requirement.

## Running & Specifying Job Parameters

To run the example job use the following command
```
qsub batchjob.pbs
```

To specify the timeout period (default 3 hours), memory used, and number of processors use the following command:
```
qsub -l walltime=hours:minutes:seconds,mem=<memory amoutn>mb,nodes=<node amount> batchjob.pbs
```

For example, this job runs for a maximum of 3 days, uses 1500mb, and uses 4 processors:
```
qsub -l walltime=72:00:00,mem=1500mb,nodes=4 diffuse.pbs
```

For advanced usage refer to http://www.democritos.it/activities/IT-MC/documentation/newinterface/pages/runningcodes.html

## Viewing Job Status

It is often necessary to view the status of jobs once they've been started.

To view all jobs currently processing use the following command:
```
showq
```

To view your own jobs use the following command:
```
qsub -l walltime=72:00:00,mem=1500mb,nodes=4 diffuse.pbs
```

Once a job has been submitted, it will take a moment to be put into the Queue, here is an example of a task in the waiting queue:
![alt tag](http://imgur.com/5EcAWrE.png)

And here is a job which is currently active:
![alt tag](http://imgur.com/k6vXecc.png)

