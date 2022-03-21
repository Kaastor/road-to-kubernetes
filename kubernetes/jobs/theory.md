# Jobs

* When a Job completes, no more Pods are created, but the Pods are usually not deleted either. 
  Keeping them around allows you to still view the logs of completed pods to check for errors, warnings, 
  or other diagnostic output. The job object also remains after it is completed so that you can view its 
  status. It is up to the user to delete old jobs after noting their status. Delete the job with kubectl.
* Finished Jobs are usually no longer needed in the system. Keeping them around in the system will put 
  pressure on the API server. If the Jobs are managed directly by a higher level controller, such as CronJobs, 
  the Jobs can be cleaned up by CronJobs based on the specified capacity-based cleanup policy.


