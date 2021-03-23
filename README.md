# This README file includes context about *FreeRTOS* 

FreeRTOS is a class of RTOS that is designed to be small enough to run on a microcontroller - although its use is not limited to microcontroller applications.

The scheduler in a Real Time Operating System (RTOS) is designed to provide a predictable (normally described as deterministic) execution pattern. This is particularly of interest
to embedded systems as embedded systems often have real time requirements.

Traditional real time schedulers, such as the scheduler used in FreeRTOS, achieve determinism by allowing the user to assign a priority to each thread of execution. The scheduler
then uses the priority to know which thread of execution to run next. In FreeRTOS, a thread of execution is called a task.

The use of a multitasking operating system can simplify the design of what would otherwise be a complex software application:
* The multitasking and inter-task communications features of the operating system allow the complex application to be partitioned into a set of smaller and more manageable tasks.
* The partitioning can result in easier software testing, work breakdown within teams, and code reuse.
* Complex timing and sequencing details can be removed from the application code and become the responsibility of the operating system.

the following picture shows cuncurrent and multitasking

![Capture](https://user-images.githubusercontent.com/80719599/112216219-df785b80-8c3e-11eb-9a7f-19ecfcae5345.PNG)

**Scheduling**

The scheduler is the part of the kernel responsible for deciding which task should be executing at any particular time. The kernel can suspend and later resume a task many times
during the task lifetime. The scheduling policy is the algorithm used by the scheduler to decide which task to execute at any point in time.

 Real time / embedded systems are designed to provide a timely response to real world events. Events occurring in the real world can have deadlines before which the real time /
 embedded system must respond and the RTOS scheduling policy must ensure these deadlines are met.
 To achieve this objective the software engineer must first assign a priority to each task. The scheduling policy of the RTOS is then to simply ensure that the highest priority
 task that is able to execute is the task given processing time. This may require sharing processing time "fairly" between tasks of equal priority if they are ready to run
 simultaneously. 
 
 


