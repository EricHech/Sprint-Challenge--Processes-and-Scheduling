1. List all of the main states a process may be in at any point in time on a standard Unix system. Briefly explain what each of these states mean.

- Start: The state of a process when it is initialized.
- Waiting: When a process is waiting from some input.
- Running: When a process is running.
- Stopped: When a process is done.
- Zombie: A process which has been finished but not yet removed.


2. What is a Zombie Process? How does it get created? How does it get destroyed?

- Processes are automatically destroyed by the reaper eventually, but when a child process is finished and the parent isn't waiting for the child, it remains in limbo until the reaper comes through. I think?


3. Describe the job of the Scheduler in the OS in general.

- The Scheduler keeps track of all the processes and tries to organize them in such a way that they are executed in the most effective way (shorter processes first, more important processes first, time-slicing processes so that bigger processes can still run and not get pushed to the end, etc.).


4. Describe the benefits of the MLFQ over a plain Round-Robin scheduler.

- A round-robin scheduler is extremely fair and therefore sacrifices some effectiveness. The MLFQ incorporates priority into the round robin, making it more effective. I think?