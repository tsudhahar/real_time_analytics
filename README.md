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

### How Real Is Real-Time?

* Real-time or near Real-time system is architectures that allow us to respond to data as we receive it without necessarily persisting it to a database first.In other words, real-time denotes the ability to process data as it arrives, rather than storing the data and retrieving it at some point in the future.
* But “the present” also has different meanings to different users. From the perspective of an online merchant, “the present” means the attention span of a potential customer. If the processing time of a transaction exceeds the customer’s attention span, the merchant doesn’t consider it real time.
* From the perspective of an options trader, however, real time means milliseconds. From the perspective of a guided missile, real time means microseconds.
* For most data analysts, real time means “pretty fast” at the data layer and “very fast” at the decision layer. “Real time is for robots,” says Joe Hellerstein, chancellor’s professor of computer science at UC Berkeley.
* _If you have people in the loop, it’s not real time. Most people take a second or two to react, and that’s plenty of time for a traditional transactional system to handle input and output_.


