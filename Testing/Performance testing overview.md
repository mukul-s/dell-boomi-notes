# Performance testing overview
Software Performance, Load & Stress Testing
Go to the profile of Nick Babich
Nick Babich
Jan 18, 2016
I found myself asking the questions about different types of testing and realized that there are so many definitions for the performance testing, but there is no simple description for the types with completely described goals and benefits.

Performance Testing
Performance testing is a general term for a testing to ascertain how a system and it’s components are performing in a particular situation. This type of testing generally does not give pass or fail results (aim is not to find defects in the application).

It’s a goal-oriented type of testing which is differ depending on system’s technology and purpose. Extremely important question before a starting of the performance session should be “Why are we performance-testing?” Answer on this question establishes a performance criteria which usually includes some of the following goals:

Concurrency (highly desirable metric if a system identifies end-users after log-in procedure) / Throughput (goal is likely to be set if the system has no concept of end-users).
Server response time (measure a time taken for one system node to respond to the request of another) / Render response time (e.g. stopwatch test of the total page rendering time) .
Performance specifications (clarify performance requirements for the system and document them in a test plan or profile).

Goal
Assuring that the system meets performance criteria. Establishing a benchmark behavior of the system.

Example
For example, for a web-based application you need to test application connection speed vs. latency by requesting a target page. Track time difference between generation of request and acknowledgement of response. And then find out performance issues, which could be related to network, software, hardware limitations, etc.

Load Testing
Load Testing is subset of performance testing. Main objective is to test by constantly and steadily increasing the load on the system till the time it reaches the threshold limit. Load testing sometimes called a volume testing or endurance testing (basically to check that the system can handle a large amount of data and sustain the continuous loads).


Goal
Expose defects in application related to buffer overflow, memory leaks and mismanagement of memory and determine the upper limit of all the components of application. Set the SLA for the application.

Example
The most common example of load testing involves subjecting a Web-based or network-based application to simultaneous hits by “thousands” of users.

Benefits
Load testing helps to determine:

Throughput
Peak production load
Hardware environment adequacy
Requirements for a load balancing
Number of concurrent users which application can handle with optimal performance results
Number of concurrent users which hardware can handle with optimal performance results
Stress Testing
Overloading existing resources in an attempt to break the system down. The main purpose behind this madness is to make sure that the system fails and recovers gracefully — this quality is known as recoverability. Stress testing sometimes includes a negative testing (removing components from the system) or fatigue testing (testing application beyond its bandwidth capacity).


Goal
The idea of this is to expose problems that do not appear under normal conditions. Define the behavior of application after failure by analysis of post-crash reports.

Example
A multi-threaded program may work fine under normal conditions but under conditions of reduced CPU availability, timing issues will be different and the application could crash. Another good example could be a number of concurrent users. An application can serve maximum user load of 1000 concurrent users, what if we double number of users with same scope of actions.

Benefits
Stress testing helps to determine:

Application errors at peak user loads
Security gaps
Hardware reaction on the overloads
Issues with data corruption
Reading & watching list

Software performance testing
Large Scale Load Testing Amazon.com’s Traffic
[Software Performance, Load & Stress Testing – Nick Babich – Medium](https://medium.com/@101/performance-load-and-stress-testing-99738e991b0e)