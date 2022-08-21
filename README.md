### Problem Statement

## Multicore Task Scheduling

In a system, there are M cores. There are N tasks which are present in the ready queue. Each
task has a different execution time (in seconds). Each core can execute a single task at a time.
Multiple cores can execute tasks simultaneously.
Each task has a priority assigned to it. The first task with a particular priority decides on which
core it can execute (say core 2). It depends on which core is free. When two or more cores are
free, a task should be executed on the core with the smaller ID. E.g. When core 3 and core 5
are free, then the task will get executed on core 3. Other tasks with the same priority
execute on the same core (eg. core 2) as the first task of that priority.
Whenever a core completes execution of a task, i.e., whenever it is free, a new task is taken
from the ready queue depending upon the task’s priority. If a task with certain priority does not
belong to that core, and if the core is free, it will be idle until the next appropriate task is taken
out. If a task with a certain priority belongs to a core and the core is busy, the task has to wait
until that particular core is free.
Since we have only one queue in the system, a task is popped out of the queue only when the
previous task is out. Thus, the ready queue is a blocking structure.

## Assumptions:
● All tasks are in the ready queue at time zero.
● All tasks are independent of each other.
● Context switching time between tasks is zero.
● Scheduling time is zero.
● The number of cores are at least as many as the number of different priorities.
