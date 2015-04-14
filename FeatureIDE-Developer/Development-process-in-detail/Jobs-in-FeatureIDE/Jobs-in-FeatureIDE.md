<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < [**FeatureIDE Developer**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Developer) < [**Development Process in detail**](https://github.com/tthuem/FeatureIDE/wiki/Development-Process-in-detail)

<!-- Introduction -->
under construction

<!-- Quick-Navigation-Table -->
### Quick-Navigation:

<table>
	<tr>
		<th>List of UIJobs</th>
		<th>List of non-UIJobs</th>
	</tr>
	<tr>
		<td width="320px">
			<p align="center">
				<img height="100" width="100" alt="under_construction" src="https://github.com/tthuem/FeatureIDE/wiki/Assets/Home/under_construction.png">
			</p>
		</td>
		<td width="320px">
			<p align="center">
				<img height="100" width="100" alt="under_construction" src="https://github.com/tthuem/FeatureIDE/wiki/Assets/Home/under_construction.png">
			</p>
		</td>
	</tr>
	<tr>
		<td>
			<!--a href="/tthuem/FeatureIDE/wiki/Checkout-FeatureIDE-sources">Checkout FeatureIDE sources</a-->
		</td>
		<td>
			<!--a href="/tthuem/FeatureIDE/wiki/Run-configuration-[FeatureIDE-Dev]">Run Configuration</a-->
		</td>
	</tr>
	<tr>
		<td>description under construction</td>
		<td>description under construction</td>
	</tr>
</table>

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

**StoppableJob**, **TreeJob** and **StoppableTreeJob** should no longer be used or extended. 


