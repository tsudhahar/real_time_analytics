## real_time_analytics

`References`

### What is Real-Time?
* A Query response in less than 20ms
  * what if:  Data is one month old
* Continuous data ingest
  * what if: Weekly/Monthly Analytics perofrmed on the data
* Online database operation
  * what if:  Completes with unreasonable latency

#### Real Time is required "Everywhere"
* Data ingestion rate
* Query response time
* Processing time
* Time to action (total time from data acquisition to business action).

The ground reality is _real time_ is required across entire process. It's time take **from** _data collected at source **to** business actionable anlytics_.

### How Real Is Real Time?
  “Typically when we’re talking about real-time or near real-time systems, what we
mean is architectures that allow you to respond to data as you receive
it without necessarily persisting it to a database first.”
In other words, real-time denotes the ability to process data as it ar‐
rives, rather than storing the data and retrieving it at some point in
the future. That’s the primary significance of the term — real-time
means that you’re processing data in the present, rather than in the
future.
But “the present” also has different meanings to different users. From
the perspective of an online merchant, “the present” means the atten‐
tion span of a potential customer. If the processing time of a transaction
exceeds the customer’s attention span, the merchant doesn’t consider
it real time.
From the perspective of an options trader, however, real time means
milliseconds. From the perspective of a guided missile, real time means
microseconds.
For most data analysts, real time means “pretty fast” at the data layer
and “very fast” at the decision layer. “Real time is for robots,” says Joe
9
Hellerstein, chancellor’s professor of computer science at UC Berkeley.
“If you have people in the loop, it’s not real time. Most people take a
second or two to react, and that’s plenty of time for a traditional trans‐
actional system to handle input and output.”
That doesn’t mean that developers have abandoned the quest for speed.
Supported by a Google grant, Matei Zaharia is working on his Ph.D.
at UC Berkeley. He is an author of Spark, an open source cluster com‐
puting system that can be programmed quickly and runs fast. Spark
relies on “resilient distributed datasets” (RDDs) and “can be used to
interactively query 1 to 2 terabytes of data in less than a second.”
In scenarios involving machine learning algorithms and other multipass
analytics algorithms, “Spark can run 10x to 100x faster than Ha‐
doop MapReduce,” says Zaharia. Spark is also the engine behind
Shark, a data warehousing system.
According to Zaharia, companies such as Conviva and Quantifind
have written UIs that launch Spark on the back end of analytics dash‐
boards. “You see the statistics on a dashboard and if you’re wondering
about some data that hasn’t been computed, you can ask a question
that goes out to a parallel computation on Spark and you get back an
answer in about half a second.”
Storm is an open source low latency processing stream processing
system designed to integrate with existing queuing and bandwidth
systems. It is used by companies such as Twitter, the Weather Channel,
Groupon and Ooyala. Nathan Marz, lead engineer at BackType (ac‐
quired by Twitter in 2011), is the author of Storm and other opensource
projects such as Cascalog and ElephantDB.
“There are really only two paradigms for data processing: batch and
stream,” says Marz. “Batch processing is fundamentally high-latency.
So if you’re trying to look at a terabyte of data all at once, you’ll never
be able to do that computation in less than a second with batch pro‐
cessing.”
Stream processing looks at smaller amounts of data as they arrive. “You
can do intense computations, like parallel search, and merge queries
on the fly,” says Marz. “Normally if you want to do a search query, you
need to create search indexes, which can be a slow process on one
machine. With Storm, you can stream the process across many ma‐
chines, and get much quicker results.”
10 | Chapter 3: How Real Is Real Time?
Twitter uses Storm to identify trends in near real time. Ideally, says
Marz, Storm will also enable Twitter to “understand someone’s intent
in virtually real time. For example, let’s say that someone tweets that
he’s going snowboarding. Storm would help you figure out which ad
would be most appropriate for that person, at just the right time.”
Storm is also relatively user friendly. “People love Storm because it’s
easy to use. It solves really hard problems such as fault tolerance and
dealing with partial failures in distributed processing. We have a plat‐
form you can build on. You don’t have to focus on the infrastructure
because that work has already been done. You can set up Storm by
yourself and have it running in minutes,” says Marz.
