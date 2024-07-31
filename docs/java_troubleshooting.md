# Comprehensive Guide to Observability in Java Applications

In the world of Java application development and operations, understanding how a
Java application is configured and operates is paramount for maintaining system
health and performance. Observability in this aspect refers to the ability to
measure and understand the internal state of an application through its external
outputs, such as metrics, profiler captures and logs. For Java applications,
effective observability involves a broad range of topics, including memory
management, thread behavior, performance metrics, error tracking, and system
resource usage. This guide attempts to provide a comprehensive overview of
these topics to help you monitor and analyze Java applications effectively.

## Memory Management and Garbage Collection

**Heap Memory**

  * Storage for Objects: The heap is where Java allocates memory for objects
created during program execution. This includes both temporary objects and
long-lived data.

  * Dynamic Memory Allocation: Java applications rely on the heap for dynamic
memory allocation, meaning objects are created and managed at runtime.

  * Heap Size Configuration: Parameters such as -Xms (initial heap size at
runtime) and -Xmx (maximum memory usage size for the heap).

**Garbage Collection (GC)**

  * GC Metrics: Monitoring metrics such as GC pause times, execution times,
frequency of GC events, and heap usage before and after GC. Currently,
frequency, heap usage and execution times are availble in DataDog.

**Memory Leaks**

  * Detection Tools: Developers usually use tools like jProfiler to identify memory
leaks and analyze heap dumps.

What Happens with Threads When GC Fails

## Minor GC Failures

**Minor GC Overview**

  * Frequency: It occurs more frequently than Major GC as it focuses on
short-lived objects.

**Thread Impact During Minor GC Failures**

  * Increased Pause Times: If minor GC fails to reclaim enough memory due
to high allocation rates or fragmentation, the JVM (Java Virtual Machine)
may experience longer pause times. Threads are paused during this
process, leading to delays in handling requests and tasks which can cause
requests and tasks to fail assuming they’re async/timeout based.

  * Thread Interruption: Threads that are executing tasks requiring memory
may be blocked or delayed while GC is in progress. This can lead to
increased response times and reduced throughput.

## Major GC Failures

**Major GC Overview**

  * Scope: Major GC (also known as Full GC) deals with the Old Generation
(Tenured space) and the entire heap. It is more comprehensive and
involves cleaning up both Young and Old Generations.

  * Frequency: It is less frequent but more resource-intensive compared to
Minor GC.

**Thread Impact During Major GC Failures**

  * Extended Pause Times: If major GC fails to reclaim sufficient memory, it
may result in extended pause times, where all application threads are
stopped. This can severely impact the application's responsiveness and
overall performance where it’s possible that the application could crash.

  * Thread Contention: Long GC pauses can cause threads to wait for
extended periods, leading to thread contention and potential bottlenecks.
Threads that are waiting for memory to become available might cause
delays in processing tasks or handling incoming requests.

  * Application Freezes: Prolonged GC pauses may lead to application
freezes or unresponsiveness, especially if the JVM cannot allocate the
required memory despite continuous GC efforts.

**General Effects of GC Failures**

  * Increased CPU Usage: Frequent and prolonged GC cycles can lead to
high CPU usage as the JVM spends more time performing garbage
collection rather than executing application code.

  * OutOfMemoryError: If GC fails to free up sufficient memory and the heap
is exhausted, the JVM may throw an OutOfMemoryError resulting in a
crash visible in the application logs. This error is indicative of impending
application crashes and/or significant instability

## Thread Management and Concurrency

**Thread States and Lifecycle**

  * Thread States: Understand the various thread states (e.g., RUNNABLE,
WAITING, BLOCKED, TIMED_WAITING).

**Thread Pools**

  * Configuration: Monitor thread pool settings, such as core pool size, maximum
pool size, and queue capacity.

  * Metrics: Track metrics like active threads, queue length, and task completion
rates.

**Concurrency Issues**

  * Deadlocks: Deadlocks occur when threads are waiting indefinitely for
resources held by each other.

  * Starvation and Livelocks: Threads are either perpetually waiting or
continuously changing states without making progress.
Thread Management and Concurrency Failure definitions and symptoms

## Thread Management and Concurrency Failure

**Deadlocks**

  * Definition: A deadlock occurs when two or more threads are each waiting
for the other to release a resource, creating a cycle of dependencies that
prevents any of them from proceeding.

  * Symptoms: Threads become stuck and do not make any progress, leading
to system stalls or unresponsiveness.

**Starvation**

  * Definition: Starvation happens when a thread is perpetually denied the
resources it needs to proceed because other threads are continually being
given priority.

  * Symptoms: The affected thread is left unable to execute, causing delays
or failures in task completion.

**Livelocks**

  * Definition: A livelock occurs when threads keep changing states in
response to each other but never make actual progress. Unlike deadlock,
threads are active but still unable to complete their tasks.

  * Symptoms: Threads keep running and interacting but fail to make
progress, leading to inefficiency and potential performance issues.

**Race Conditions**

  * Definition: A race condition happens when multiple threads access shared
data concurrently, and the final outcome depends on the unpredictable
order of access.

  * Symptoms: Erratic behavior or incorrect results due to unsynchronized
access to shared resources.

**Thread Contention**

  * Definition: Thread contention arises when multiple threads compete for
the same resources, leading to delays and reduced performance.

  * Symptoms: Increased context switching, longer execution times, and
reduced overall throughput.

**Resource Leaks**

  * Definition: Resource leaks occur when threads fail to release resources
(like locks, file handles, or memory) properly, causing resources to be held
longer than necessary.

  * Symptoms: Resource exhaustion/overconsumption, leading to degraded
performance or system crashes.

## Application Performance Metrics

**Response Time**

  * Latency: Measures latency for various types of requests (e.g., HTTP requests,
database queries).

**Throughput and Tolerance**

  * Request Rate: Tracks the number of requests processed by the appliation in a
given unit of time (usually millisecond).

  * Load Testing: Conduct load testing to understand application behavior under
stress and high traffic.

**Error Rates and types**

  * Exception Tracking: Monitor the frequency and types of exceptions occurring
in the application.

  * Types:
    1. Null Pointer Exception (NPE) - 
    Cause: Attempting to use an object reference that has not been initialized (i.e.,it is null ).
    1. IllegalArgumentException - 
    Cause: Passing an illegal or inappropriate argument to a method.
    1. IOException - 
    Cause: Errors related to input and output operations, such as file reading/writing issues.

Note: There are many many more but these are the few I have
notes/documentation/experience with.

##System Resource Utilization

**CPU Usage**

  * Profiling: Developers use profiling tools like jProfiler to measure CPU usage
and identify hotspots.

  * Resource Contention: This is where multiple threads or processes compete
for resources.

**Disk I/O**

  * I/O Metrics: Track read and write operations, disk usage, and file system
performance.

  * Database I/O: Monitor database interaction patterns and optimize queries to
reduce impact on I/O load.

**Network Traffic**

  * Traffic Analysis: Measures inbound and outbound network traffic and latency.

  * Network Latency: Monitor for network latency and bandwidth usage,
especially for applications with significant network communication.

**Logging**

  * Log Levels: Developers set different logging levels (verbosity from highest

  * lowest: e.g., TRACE, DEBUG, INFO, WARN, ERROR) to capture the right amount
of information depending on the importance of the actions being taken without
filling up log storage needlessly. This helps in troubleshooting and pinpointing
issues related to the application's functionality.

## Application Resilience

**Fault Tolerance**

  * Retries and Timeouts: A developer will configure retries and timeouts for
failures and ensure they are handled gracefully. Typically these retries and
timeouts are printed in the application logs.
