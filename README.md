### AWS Cloud Cost Optimization - Identifying Stale Resources

#### Identifying Stale EBS Snapshots

I'm creating a Lambda function to identify and delete EBS snapshots that are no longer associated with any active EC2 instances, aiming to save on storage costs.

#### Description:

This Lambda function fetches all EBS snapshots owned by my account and retrieves a list of active EC2 instances, both running and stopped. For each snapshot, it checks if the associated volume exists and whether it is linked to any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing my storage costs.
