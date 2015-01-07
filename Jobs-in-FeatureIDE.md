Eclipse jobs exist to keep long-running processes from blocking the main thread. For an introduction on this topic you can refer to the Vogella tutorial ([here](http://www.vogella.com/tutorials/EclipseJobs/article.html)).
For FeatureIDE development classes with additional functionality have been implemented. 

* **AMonitorJob**: Implements monitoring for **AChainJob**
* **AJob**: Implements support for the **JobFinishListener**. Default priority is Job.SHORT
* **AStoppableJob**: Abstract class for Jobs that might have to be stopped. Also supports the **JobFinishListener**
* **AChainJob**: A Job that starts another job when it is done
* **AWaitingJob**: If this job is scheduled twice, the second will be called after the first one is finished. As long as there is still a job waiting, all further calls to schedule() are ignored

**AbstractJob** is used for the implementation of **AJob** and **AStoppableJob** and usually should not be extended directly.

###Interfaces###

The following interfaces are defined on FeatureIDE-specific jobs: **IJob, IStoppableJob, IChainJob**.

###Deprecation###

**TreeJob** should no longer be used or extended. 