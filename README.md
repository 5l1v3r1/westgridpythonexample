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
