# preemptive scheduling 和 time slicing?

preemptive scheduling,
优先级别最高的任务会被执行,
除非它进入等待状态或者死了或者一个更高优先权的任务进来.

time slicing,
a task executes for a predefined slice of time and then reenters the pool of ready tasks. The scheduler then determines which task should execute next, based on priority and other factors.
