# Improved-Scheduling-Algorithm-for-Soft-Real-Time-Systems


# Introduction
We have tried to come up with a modified round robin scheduling algorithm which is a combination of round robin scheduler and priority scheduler. It works on a dynamic time quantum, which changes after every round of execution. This will help in reducing the average waiting time, average turnaround time and reduce the number of context switch.

# Solution
We calculate an intelligent time slice (ITS) is calculated based on the priority, shortest CPU burst time and context switch. We have a pre-defined time slice which is the original time slice (OTS), if the process needs special consideration, the priority component (PC) is assigned to 0 or 1 according to the pre-defined priority by the user. We define a Shortness component (SC) which is the difference between the burst time of the current process and its previous process. If the difference is negative, we make SC as 1 else 0. To calculate CSC i.e., Context switch component we add PC, SC and OTP and the resulting sum is subtracted from the burst time of the process. If the result obtained is less than the OTS, we consider it as CSC. Adding all the calculated components we get our ITS.
Time quantum varies from TQi to TQn, where i is the round number.

