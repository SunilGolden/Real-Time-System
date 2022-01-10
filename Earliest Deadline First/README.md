# Earliest Deadline First 

Earliest Deadline First (EDF) is an optimal dynamic priority scheduling algorithm used in real-time systems.
It can be used for both **static** and **dynamic real-time scheduling**.

EDF uses priorities to the jobs for scheduling. It assigns priorities to the task according to the absolute deadline. The task whose deadline is closest gets the highest priority. The priorities are assigned and changed in a dynamic fashion. EDF is very efficient as compared to other scheduling algorithms in real-time systems. It can make the CPU utilization to about 100% while still guaranteeing the deadlines of all the tasks.

[ [Source] ](https://www.geeksforgeeks.org/earliest-deadline-first-edf-cpu-scheduling-algorithm/)