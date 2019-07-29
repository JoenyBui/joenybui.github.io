---

---

# Data-Intensive

* Store data so that they, or another application, can find it again later (databases)
* Remember the result of an expensive operation, to speed up reads (caches)
* Allow users to search data by keyword or filter it in various ways (searches indexes)
* Send a message to another process, to be handled asynchronously (message queues)
* Observe what is happening, and act on events as they occur (stream processing)
* Periodically crunch a large amount of accumalted data (batch processing)

1. Relaibility
* tolerating hardware & software faults
* human errors
2. Scalability
* measuring load & performance
* latency percentiles, throughput
3. Maintainability
* operability
* simplicity
* evolvability

## Questions

* How do you ensure that the data remains correct and cmoplete, even when things go wrong internally?
* How do you provide consistently good performance to clients, even when parts of your system are degraded?
* How do you scale to handle an increase in load?
* What does a good API for the service look like?

## Reliability

* *Fault* is not the same as *failure*.  A *fault* is usually deifned as one component of the system deviating from its spec, whereas a *failure* is when the system as a whole stops providing the required service to the user.
* It might be beneficial to test you system by introducing *faults* - see **Chaos Monkey**.


## Monotonic Read

Monotoic reads is a gurantee that this kind of anomaly does not happen where the user will read from different replications  It's a lesser gurantee than strong consistency, but a stronger gurantee then eventual consistency.  One way to of achieving monotonic reads is to make sure that each reads from the same replica (you can read from the same replica).

## Consistent Prefix Reads

This guranteeds says that if a sequence of writes happends in a certain order, then anyone reading those writes will see them appear in the same order.  A particular problem in partition (sharded) databases.  

## Multiple-Leader Replicaiton

Allows multiple leaders to write to database and then replicated across systems.
