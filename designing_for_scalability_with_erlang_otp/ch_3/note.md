OTP provides a powerful, reusable solution at location 1396
 
Be spawned and initialized Repeatedly receive messages, handle them, and send replies Be terminated (normally or abnormally)
at location 1403

Figure 3-1 shows a typical process flow diagram outlining the lifecycle of a process. at location 1427

sending a client request to a server will be generic. at location 1467

The idea behind OTP behaviors is to split up the code into two modules: one for the generic pattern, referred to as the
behavior module, and one for specifics, referred to as the callback module at location 1483

OTP provides five behaviors that cover the majority of all cases. at location 1494

Using behaviors, we are reducing the code base while creating a standardized programming style at location 1516

The small increase in memory usage and reduction in performance is a small price to pay for reliability and fault tolerance.
The rule of thumb is to always start with behaviors, and optimize when bottlenecks occur. at location 1534

start and stop servers, at location 1595

Although starting the server, spawning the server process, and registering it are generic, the registered name and module
containing the init function are considered specific. at location 1619

So, which parts of the code are generic? Which will not change from one client-server implementation to another? 
at location 1679

For starters, looping is generic. The protocol used to send and receive messages is generic, but the messages and replies
themselves aren’t. Finally, stopping the server is generic, as is acknowledging the stop message. at location 1748
