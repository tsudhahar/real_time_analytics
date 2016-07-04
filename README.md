## Real-Time Big Data Analytics (RTBDA)

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

### The RTBDA Stack

* There is presently no one-size-fits-all model, which
makes sense when you consider that the interrelationships among
people, processes and technologies within the RTBDA universe are
still evolving.
* David Smith writes a popular blog for Revolution Analytics on open
source R, a programming language designed specifically for data an‐
alytics. He proposes a four-layer RTBDA technology stack. Although
his stack is geared for predictive analytics, it serves as a good general
model.
From David Smith’s presentation, [“Real-Time Big Data Analytics: From Deployment To Production”](http://www.revolutionanalytics.com/webinars/real-time-big-data-analytics-deployment-production): 
![alt text](https://github.com/tsudhahar/real_time_analytics/blob/master/references/rtbda_stack_r.PNG "Real-Time Big Data Analytics: From Deployment To Production")

##### Data Layer
* At the foundation is the data layer. At this level you have structured
data in an RDBMS, NoSQL, Hbase, or Impala; unstructured data in
Hadoop MapReduce; streaming data from the web, social media, sen‐
sors and operational systems; and limited capabilities for performing
descriptive analytics. Tools such as Hive, HBase, Storm and Spark also
sit at this layer. (Matei Zaharia suggests dividing the data layer into
two layers, one for storage and the other for query processing)

##### Analytics Layer
* The analytics layer sits above the data layer. The analytics layer in‐
cludes a production environment for deploying real-time scoring and
dynamic analytics; a development environment for building models;
and a local data mart that is updated periodically from the data layer,
situated near the analytics engine to improve performance.



##### Integration Layer
* On top of the analytics layer is the integration layer. It is the “glue” that
holds the end-user applications and analytics engines together, and it
usually includes a rules engine or CEP engine, and an API for dynamic
analytics that “brokers” communication between app developers and
data scientists.

##### Decision Layer
* The topmost layer is the decision layer. This is where the rubber meets
the road, and it can include end-user applications such as desktop,
mobile, and interactive web apps, as well as business intelligence soft‐
ware. This is the layer that most people “see.” It’s the layer at which
business analysts, c-suite executives, and customers interact with the
real-time big data analytics system.

Again, it’s important to note that each layer is associated with different
sets of users, and that different sets of users will define “real time”
differently. Moreover, the four layers aren’t passive lumps of technol‐
ogies — each layer enables a critical phase of real-time analytics de‐
ployment.

