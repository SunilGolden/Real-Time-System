# Preemptive Priority Scheduling

In Preemptive Priority Scheduling, at the time of arrival of a process in the ready queue, its Priority is compared with the priority of the other processes present in the ready queue as well as with the one which is being executed by the CPU at that point of time. The One with the highest priority among all the available processes will be given the CPU next.

The difference between preemptive priority scheduling and non preemptive priority scheduling is that, in the preemptive priority scheduling, the job which is being executed can be stopped at the arrival of a higher priority job.

Once all the jobs get available in the ready queue, the algorithm will behave as non-preemptive priority scheduling, which means the job scheduled will run till the completion and no preemption will be done.

[ [Source] ](https://www.javatpoint.com/os-preemptive-priority-scheduling)

# Algorithm

```python
completed = 0
current_time = 0

while (completed != n) {
    find process with maximum priority time among process that are in ready queue at current_time
    
    if(process found) {
        if(process is getting CPU for the first time) {
            start_time = current_time
        }
        
        burst_time = burst_time - 1
        current_time = current_time + 1
        
        if (burst_time == 0) {
            completion_time  = current_time
            turnaround_time = completion_time - arrival_time
            waiting_time = turnaround_time - burst_time
            response_time = start_time - arrival_time

            mark process as completed
            completed++
        }
    }
    else {
        current_time++
    }
}
```


# Formula

```
TAT = CT - AT
WT = TAT - BT
RT = ST - AT
```

```
AT - Arrival Time of the process
BT - Burst time of the process
ST - Start time of the process
CT - Completion time of the process
TAT - Turnaround time of the process
WT - Waiting time of the process
RT - Response time of the process
```