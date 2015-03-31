

# Introduction #

This page is intended as a resource for people writing papers that refer to the Google cluster traces.  It is intended to cover papers that analyze the traces, as well as ones that use them as inputs to other studies.

  * It's recommended to `\usepackage{url`}.
  * Entries are in publication-date order, with the most recent at the top.
  * Items in **bold** are the recommended citations.
  * Bibtex ignores stuff that is outside the entries, so it's safe to copy and save the entire contents as a .bib file.

# Trace-announcements #
These entries can be used to cite the traces themselves.
The first couple are for the May 2011 "full" trace.
<pre>
@Misc{clusterdata:Wilkes2011,<br>
author = {John Wilkes},<br>
title = {More {Google} cluster data},<br>
howpublished = {Google research blog},<br>
month = Nov,<br>
year = 2011,<br>
note = {Posted at \url{http://googleresearch.blogspot.com/2011/11/more-google-cluster-data.html}.},<br>
}<br>
</pre>

<pre>
@TechReport{clusterdata:Reiss2011,<br>
author = {Charles Reiss and John Wilkes and Joseph L. Hellerstein},<br>
title = {{Google} cluster-usage traces: format + schema},<br>
institution = {Google Inc.},<br>
year = 2011,<br>
month = Nov,<br>
type = {Technical Report},<br>
address = {Mountain View, CA, USA},<br>
note = {Revised 2012.03.20.  Posted at URL<br>
\url{http://code.google.com/p/googleclusterdata/wiki/TraceVersion2}},<br>
}<br>
</pre>

The second one is for the "small" 7-hour trace that was released first.
<pre>
@Misc{clusterdata:Hellersetein2010,<br>
author = {Joseph L. Hellerstein},<br>
title = {{Google} cluster data},<br>
howpublished = {Google research blog},<br>
month = Jan,<br>
year = 2010,<br>
note = {Posted at \url{http://googleresearch.blogspot.com/2010/01/google-cluster-data.html}.},<br>
}<br>
</pre>

The next paper describes the policy choices and technologies used to
make the traces safe to release.
<pre>
@InProceedings{clusterdata:Reiss2012,<br>
author = {Charles Reiss and John Wilkes and Joseph L. Hellerstein},<br>
title = {Obfuscatory obscanturism: making workload traces of<br>
commercially-sensitive systems safe to release},<br>
year = 2012,<br>
booktitle = {3rd International Workshop on Cloud Management (CLOUDMAN)},<br>
month = Apr,<br>
publisher = {IEEE},<br>
pages = {1279--1286},<br>
address = {Maui, HI, USA},<br>
abstract = {Cloud providers such as Google are interested in<br>
fostering research on the daunting technical challenges they<br>
face in supporting planetary-scale distributed systems, but no<br>
academic organizations have similar scale systems on which to<br>
experiment. Fortunately, good research can still be done using<br>
traces of real-life production workloads, but there are risks<br>
in releasing such data, including inadvertently disclosing<br>
confidential or proprietary information, as happened with the<br>
Netflix Prize data. This paper discusses these risks, and our<br>
approach to them, which we call systematic obfuscation. It<br>
protects proprietary and personal data while leaving it<br>
possible to answer interesting research questions. We explain<br>
and motivate some of the risks and concerns and propose how<br>
they can best be mitigated, using as an example our recent<br>
publication of a month-long trace of a production system<br>
workload on a 11k-machine cluster.},<br>
url = {http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=6212064},<br>
}<br>
</pre>

# Trace-analysis papers #

These papers are primarily about analyzing the traces.  **If you just want one citation, then `\cite{clusterdata:Reiss2012b}` is recommended.**   Order: most recent first.

<pre>
@INPROCEEDINGS{clusterdata:Abdul-Rahman2014,<br>
author = {Abdul-Rahman, Omar Arif and Aida, Kento},<br>
title = {Towards understanding the usage behavior of {Google} cloud users: the mice and elephants phenomenon},<br>
booktitle = {IEEE International Conference on Cloud Computing Technology and Science (CloudCom)},<br>
year = 2014,<br>
month = dec,<br>
address = {Singapore},<br>
pages = {272--277},<br>
keywords = { Google trace; Workload trace analysis; User session<br>
view; Application composition; Mass-Count disparity;<br>
Exploratory statistical analysis; Visual analysis;<br>
Color-schemed graphs; Coarse grain classification;<br>
Heavy-tailed distributions; Long-tailed lognormal<br>
distributions; Exponential distribution; Normal distribution;<br>
Discrete modes; Large web services; Batch processing;<br>
MapReduce computation; Human users; },<br>
abstract = {In the era of cloud computing, users encounter the<br>
challenging task of effectively composing and running their<br>
applications on the cloud. In an attempt to understand user<br>
behavior in constructing applications and interacting with<br>
typical cloud infrastructures, we analyzed a large utilization<br>
dataset of Google cluster. In the present paper, we consider<br>
user behavior in composing applications from the perspective<br>
of topology, maximum requested computational resources, and<br>
workload type. We model user dynamic behavior around the<br>
user's session view. Mass-Count disparity metrics are used to<br>
investigate the characteristics of underlying statistical<br>
models and to characterize users into distinct groups<br>
according to their composition and behavioral classes and<br>
patterns. The present study reveals interesting insight into<br>
the heterogeneous structure of the Google cloud workload.},<br>
doi={10.1109/CloudCom.2014.75},<br>
}<br>
</pre>

<pre>
@inproceedings{clusterdata:Di2013,<br>
title = {Characterizing cloud applications on a {Google} data center},<br>
author = {Di, Sheng and Kondo, Derrick and Franck, Cappello},<br>
booktitle = {42nd International Conference on Parallel Processing (ICPP)},<br>
year = 2013,<br>
month = Oct,<br>
address = {Lyon, France},<br>
abstract = {In this paper, we characterize Google applications,<br>
based on a one-month Google trace with over 650k jobs running<br>
across over 12000 heterogeneous hosts from a Google data<br>
center. On one hand, we carefully compute the valuable<br>
statistics about task events and resource utilization for<br>
Google applications, based on various types of resources (such<br>
as CPU, memory) and execution types (e.g., whether they can<br>
run batch tasks or not). Resource utilization per application<br>
is observed with an extremely typical Pareto principle. On the<br>
other hand, we classify applications via a K-means clustering<br>
algorithm with optimized number of sets, based on task events<br>
and resource usage. The number of applications in the Kmeans<br>
clustering sets follows a Pareto-similar distribution. We<br>
believe our work is very interesting and valuable for the<br>
further investigation of Cloud environment.},<br>
}<br>
</pre>

<pre>
@INPROCEEDINGS{clusterdata:Reiss2012b,<br>
title = {Heterogeneity and dynamicity of clouds at scale:<br>
{Google} trace analysis},<br>
author = {Charles Reiss and Alexey Tumanov and Gregory R. Ganger and<br>
Randy H. Katz and Michael A. Kozuch},<br>
booktitle = {ACM Symposium on Cloud Computing (SoCC)},<br>
year = 2012,<br>
month = Oct,<br>
address = {San Jose, CA, USA},<br>
abstract = {To better understand the challenges in developing<br>
effective cloud-based resource schedulers, we analyze the first<br>
publicly available trace data from a sizable multi-purpose cluster.<br>
The most notable workload characteristic is heterogeneity: in<br>
resource types (e.g., cores:RAM per machine) and their usage<br>
(e.g., duration and resources needed). Such heterogeneity reduces<br>
the effectiveness of traditional slot- and core-based scheduling.<br>
Furthermore, some tasks are constrained as to the kind of machine<br>
types they can use, increasing the complexity of resource assignment<br>
and complicating task migration. The workload is also highly<br>
dynamic, varying over time and most workload features, and is<br>
driven by many short jobs that demand quick scheduling decisions.<br>
While few simplifying assumptions apply, we find that many<br>
longer-running jobs have relatively stable resource utilizations,<br>
which can help adaptive resource schedulers.},<br>
url = {http://www.pdl.cmu.edu/PDL-FTP/CloudComputing/googletrace-socc2012.pdf},<br>
privatenote = {An earlier version of this was posted at<br>
\url{http://www.istc-cc.cmu.edu/publications/papers/2012/ISTC-CC-TR-12-101.pdf},<br>
and included here as clusterdata:Reiss2012a. Please use this<br>
version instead of that.},<br>
}<br>
</pre>

<pre>
@INPROCEEDINGS{clusterdata:Liu2012,<br>
author = {Zitao Liu and Sangyeun Cho},<br>
title = {Characterizing machines and workloads on a {Google} cluster},<br>
booktitle = {8th International Workshop on Scheduling and Resource Management<br>
for Parallel and Distributed Systems (SRMPDS)},<br>
year = 2012,<br>
month = Sep,<br>
address = {Pittsburgh, PA, USA},<br>
abstract = {Cloud computing offers high scalability, flexibility and<br>
cost-effectiveness to meet emerging computing<br>
requirements. Understanding the characteristics of real<br>
workloads on a large production cloud cluster benefits not<br>
only cloud service providers but also researchers and daily<br>
users.  This paper studies a large-scale Google cluster usage<br>
trace dataset and characterizes how the machines in the<br>
cluster are managed and the workloads submitted during a<br>
29-day period behave. We focus on the frequency and pattern of<br>
machine maintenance events, job- and task-level workload<br>
behavior, and how the overall cluster resources are utilized.},<br>
url = {http://www.cs.pitt.edu/cast/abstract/liu-srmpds12.html},<br>
}<br>
</pre>

<pre>
@INPROCEEDINGS{clusterdata:Di2012a,<br>
author = {Sheng Di and Derrick Kondo and Walfredo Cirne},<br>
title = {Characterization and comparison of cloud versus {Grid} workloads},<br>
booktitle = {International Conference on Cluster Computing (IEEE CLUSTER)},<br>
year = 2012,<br>
month = Sep,<br>
pages = {230--238},<br>
address = {Beijing, China},<br>
abstract = {A new era of Cloud Computing has emerged, but the<br>
characteristics of Cloud load in data centers is not perfectly<br>
clear. Yet this characterization is critical for the design of<br>
novel Cloud job and resource management systems. In this<br>
paper, we comprehensively characterize the job/task load and<br>
host load in a real-world production data center at Google<br>
Inc. We use a detailed trace of over 25 million tasks across<br>
over 12,500 hosts. We study the differences between a Google<br>
data center and other Grid/HPC systems, from the perspective<br>
of both work load (w.r.t. jobs and tasks) and host load<br>
(w.r.t. machines). In particular, we study the job length, job<br>
submission frequency, and the resource utilization of jobs in<br>
the different systems, and also investigate valuable<br>
statistics of machine's maximum load, queue state and relative<br>
usage levels, with different job priorities and resource<br>
attributes. We find that the Google data center exhibits finer<br>
resource allocation with respect to CPU and memory than that<br>
of Grid/HPC systems. Google jobs are always submitted with<br>
much higher frequency and they are much shorter than Grid<br>
jobs. As such, Google host load exhibits higher variance and<br>
noise.},<br>
keywords={cloud computing;computer centres;grid computing;queueing<br>
theory;resource allocation;search engines;CPU;Google data<br>
center;cloud computing;cloud job;cloud load;data centers;grid<br>
workloads;grid-HPC systems;host load;job length;job submission<br>
frequency;jobs resource utilization;machine maximum load;queue<br>
state;real-world production data center;relative usage<br>
levels;resource allocation;resource attributes;resource<br>
management systems;task load;Capacity<br>
planning;Google;Joints;Load modeling;Measurement;Memory<br>
management;Resource management;Cloud Computing;Grid<br>
Computing;Load Characterization},<br>
doi = {10.1109/CLUSTER.2012.35},<br>
privatenote = {An earlier version is available at<br>
\url{http://hal.archives-ouvertes.fr/hal-00705858}.<br>
It used to be included here as clusterdata:Di2012.},<br>
}<br>
</pre>

<pre>
@Article{clusterdata:Mishra2010,<br>
author = {Mishra, Asit K. and Hellerstein, Joseph L. and Cirne, Walfredo and<br>
Das, Chita R.},<br>
title = {Towards characterizing cloud backend workloads: insights from<br>
{Google} compute clusters},<br>
journal = {SIGMETRICS Perform. Eval. Rev.},<br>
volume = {37},<br>
number = {4},<br>
month = Mar,<br>
year = 2010,<br>
issn = {0163-5999},<br>
pages = {34--41},<br>
numpages = {8},<br>
url = {http://doi.acm.org/10.1145/1773394.1773400},<br>
doi = {10.1145/1773394.1773400},<br>
publisher = {ACM},<br>
abstract = {The advent of cloud computing promises highly available,<br>
efficient, and flexible computing services for applications<br>
such as web search, email, voice over IP, and web search<br>
alerts. Our experience at Google is that realizing the<br>
promises of cloud computing requires an extremely scalable<br>
backend consisting of many large compute clusters that are<br>
shared by application tasks with diverse service level<br>
requirements for throughput, latency, and jitter. These<br>
considerations impact (a) capacity planning to determine which<br>
machine resources must grow and by how much and (b) task<br>
scheduling to achieve high machine utilization and to meet<br>
service level objectives.<br>
<br>
Both capacity planning and task scheduling require a<br>
good understanding of task resource consumption (e.g., CPU and<br>
memory usage). This in turn demands simple and accurate<br>
approaches to workload classification-determining how to form<br>
groups of tasks (workloads) with similar resource demands. One<br>
approach to workload classification is to make each task its<br>
own workload. However, this approach scales poorly since tens<br>
of thousands of tasks execute daily on Google compute<br>
clusters. Another approach to workload classification is to<br>
view all tasks as belonging to a single<br>
workload. Unfortunately, applying such a coarse-grain workload<br>
classification to the diversity of tasks running on Google<br>
compute clusters results in large variances in predicted<br>
resource consumptions.<br>
<br>
This paper describes an approach to workload<br>
classification and its application to the Google Cloud<br>
Backend, arguably the largest cloud backend on the planet. Our<br>
methodology for workload classification consists of: (1)<br>
identifying the workload dimensions; (2) constructing task<br>
classes using an off-the-shelf algorithm such as k-means; (3)<br>
determining the break points for qualitative coordinates<br>
within the workload dimensions; and (4) merging adjacent task<br>
classes to reduce the number of workloads. We use the<br>
foregoing, especially the notion of qualitative coordinates,<br>
to glean several insights about the Google Cloud Backend: (a)<br>
the duration of task executions is bimodal in that tasks<br>
either have a short duration or a long duration; (b) most<br>
tasks have short durations; and (c) most resources are<br>
consumed by a few tasks with long duration that have large<br>
demands for CPU and memory.},<br>
}<br>
</pre>


---


# Trace-usage papers #

These entries are for papers that primarily focus on some other
topic, but use the traces as inputs, e.g., in simulations or load predictions.  Order: most recent first.

<pre>
@InProceedings{clusterdata:Iglesias2014:task-estimation,<br>
author = {Jesus Omana Iglesias and Liam Murphy Lero and Milan De Cauwer<br>
and Deepak Mehta and Barry O'Sullivan},<br>
title = {A methodology for online consolidation of tasks through more accurate<br>
resource estimations}<br>
year = 2014,<br>
month = Dec,<br>
booktitle = {IEEE/ACM Intl. Conf. on Utility and Cloud Computing (UCC)},<br>
address = {London, UK},<br>
abstract={Cloud providers aim to provide computing services for a<br>
wide range of applications, such as web applications, emails,<br>
web searches, and map reduce jobs. These applications are<br>
commonly scheduled to run on multi-purpose clusters that<br>
nowadays are becoming larger and more heterogeneous. A major<br>
challenge is to efficiently utilize the cluster's available<br>
resources, in particular to maximize overall machine<br>
utilization levels while minimizing application waiting<br>
time. We studied a publicly available trace from a large<br>
Google cluster ($\sim$12,000 machines) and observed that users<br>
generally request more resources than required for running<br>
their tasks, leading to low levels of utilization.  In this<br>
paper, we propose a methodology for achieving an efficient<br>
utilization of the cluster's resources while providing the<br>
users with fast and reliable computing services. The<br>
methodology consists of three main modules: i) a prediction<br>
module that forecasts the maximum resource requirement of a<br>
task; ii) a scalable scheduling module that efficiently<br>
allocates tasks to machines; and iii) a monitoring module that<br>
tracks the levels of utilization of the machines and tasks. We<br>
present results that show that the impact of more accurate<br>
resource estimations for the scheduling of tasks can lead to<br>
an increase in the average utilization of the cluster, a<br>
reduction in the number of tasks being evicted, and a<br>
reduction in task waiting time.},<br>
keys = {online scheduling, Cloud computing, forecasting, resource provisioning,<br>
constraint programming},<br>
}<br>
</pre>

<pre>
@InProceedings{clusterdata:Balliu2014,<br>
author = {Alkida Balliu and Dennis Olivetti and Ozalp Babaoglu and<br>
Moreno Marzolla and Alina Sirbu},<br>
title = {{BiDAl: Big Data Analyzer} for cluster traces},<br>
year = 2014,<br>
booktitle = {Informatik Workshop on System Software Support for Big Data (BigSys)},<br>
month = Sep,<br>
publisher = {GI-Edition Lecture Notes in Informatics},<br>
abstract = {<br>
Modern data centers that provide Internet-scale<br>
services are stadium-size structures housing tens of<br>
thousands of heterogeneous devices (server clusters,<br>
networking equipment, power and cooling infrastructures)<br>
that must operate continuously and reliably.  As part of<br>
their operation, these devices produce large amounts of<br>
data in the form of event and error logs that are<br>
essential not only for identifying problems but also for<br>
improving data center efficiency and management. These<br>
activities employ data analytics and often exploit hidden<br>
statistical patterns and correlations among different<br>
factors present in the data.  Uncovering these patterns<br>
and correlations is challenging due to the sheer volume<br>
of data to be analyzed. This paper presents BiDAl, a<br>
prototype ``log-data analysis framework'' that<br>
incorporates various Big Data technologies to simplify<br>
the analysis of data traces from large clusters. BiDAl is<br>
written in Java with a modular and extensible<br>
architecture so that different storage<br>
backends (currently, HDFS and SQLite are supported), as<br>
well as different analysis languages (current<br>
implementation supports SQL, R and Hadoop MapReduce) can<br>
be easily selected as appropriate. We present the design<br>
of BiDAl and describe our experience using it to analyze<br>
several public traces of Google data clusters for<br>
building a simulation model capable of reproducing<br>
observed behavior.},<br>
}<br>
</pre>

<pre>
@inproceedings{clusterdata:Caglar2014,<br>
title = {{iOverbook}: intelligent resource-overbooking to support soft<br>
real-time applications in the cloud},<br>
author = {Faruk Caglar and Aniruddha Gokhale},<br>
booktitle = {7th IEEE International Conference on Cloud Computing (IEEE CLOUD)},<br>
year = 2014,<br>
month = {Jun--Jul},<br>
address = {Anchorage, AK, USA},<br>
abstract = {<br>
Cloud service providers (CSPs) often overbook their<br>
resources with user applications despite having to maintain<br>
service-level agreements with their customers. Overbooking is<br>
attractive to CSPs because it helps to reduce power consumption<br>
in the data center by packing more user jobs in less number of<br>
resources while improving their profits. Overbooking becomes<br>
feasible because user applications tend to overestimate their<br>
resource requirements utilizing only a fraction of the allocated<br>
resources. Arbitrary resource overbooking ratios, however, may<br>
be detrimental to soft real-time applications, such as airline<br>
reservations or Netflix video streaming, which are increasingly<br>
hosted in the cloud. The changing dynamics of the cloud preclude<br>
an offline determination of overbooking ratios. To address these<br>
concerns, this paper presents iOverbook, which uses a machine<br>
learning approach to make systematic and online determination<br>
of overbooking ratios such that the quality of service needs of<br>
soft real-time systems can be met while still benefiting from<br>
overbooking. Specifically, iOverbook utilizes historic data of<br>
tasks and host machines in the cloud to extract their resource<br>
usage patterns and predict future resource usage along with the<br>
expected mean performance of host machines. To evaluate our<br>
approach, we have used a large usage trace made available by<br>
Google of one of its production data centers. In the context of<br>
the traces, our experiments show that iOverbook can help CSPs<br>
improve their resource utilization by an average of 12.5\% and<br>
save 32\% power in the data center.},<br>
url = {http://www.dre.vanderbilt.edu/~gokhale/WWW/papers/CLOUD-2014.pdf},<br>
}<br>
</pre>

<pre>
@inproceedings{clusterdata:Sebastio2014,<br>
author = {Sebastio, Stefano and Amoretti, Michele and Lluch Lafuente, Alberto},<br>
title = {A computational field framework for collaborative task execution in<br>
volunteer clouds},<br>
booktitle = {International Symposium on Software Engineering for Adaptive<br>
and Self-Managing Systems (SEAMS)},<br>
year = 2014,<br>
month = Jun,<br>
isbn = {978-1-4503-2864-7},<br>
address = {Hyderabad, India},<br>
pages = {105--114},<br>
url = {http://doi.acm.org/10.1145/2593929.2593943},<br>
doi = {10.1145/2593929.2593943},<br>
publisher = {ACM},<br>
keywords = {ant colony optimization, bio-inspired algorithms, cloud computing,<br>
distributed tasks execution, peer-to-peer, self-* systems, spatial computing,<br>
volunteer computing},<br>
abstract = {The increasing diffusion of cloud technologies offers new opportunities<br>
for distributed and collaborative computing. Volunteer clouds are a prominent example,<br>
where participants join and leave the platform and collaborate by sharing computational<br>
resources. The high complexity, dynamism and unpredictability of such scenarios call<br>
for decentralized self-* approaches. We present in this paper a framework for the design<br>
and evaluation of self-adaptive collaborative task execution strategies in volunteer clouds.<br>
As a byproduct, we propose a novel strategy based on the Ant Colony Optimization<br>
paradigm, that we validate through simulation-based statistical analysis over Google<br>
cluster data.},<br>
}<br>
</pre>

<pre>
@inproceedings{clusterdata:Breitgand2014-adaptive,<br>
title = {An adaptive utilization accelerator for virtualized environments},<br>
author = {Breitgand, David and Dubitzky, Zvi and Epstein, Amir and Feder, Oshrit and<br>
Glikson, Alex and Shapira, Inbar and Toffetti, Giovanni},<br>
booktitle = {International Conference on Cloud Engineering (IC2E)},<br>
pages = {165--174},<br>
year = 2014,<br>
month = Mar,<br>
publisher = IEEE,<br>
address = {Boston, MA, USA},<br>
abstract = { One of the key enablers of a cloud provider competitiveness is<br>
ability to over-commit shared infrastructure at ratios that are higher<br>
than those of other competitors, without compromising non-functional<br>
requirements, such as performance. A widely recognized impediment to<br>
achieving this goal is so called ``Virtual Machines sprawl'', a phenomenon<br>
referring to the situation when customers order Virtual Machines (VM) on<br>
the cloud, use them extensively and then leave them inactive for<br>
prolonged periods of time. Since a typical cloud provisioning system<br>
treats new VM provision requests according to the nominal virtual<br>
hardware specification, an often occurring situation is that the nominal<br>
resources of a cloud/pool become exhausted fast while the physical hosts<br>
utilization remains low. We present IBM adaPtive UtiLiSation AcceleratoR<br>
(IBM PULSAR), a cloud resources scheduler that extends OpenStack Nova<br>
Filter Scheduler. IBM PULSAR recognises that effective safely attainable<br>
over-commit ratio varies with time due to workloads' variability and<br>
dynamically adapts the effective over-commit ratio to these changes.},<br>
}<br>
</pre>

<pre>
@ARTICLE{clusterdata:Zhang2014-Harmony,<br>
author={Qi Zhang and Mohamed Faten Zhani and Raouf Boutaba and<br>
Joseph L Hellerstein},<br>
title={Dynamic heterogeneity-aware resource provisioning in the cloud},<br>
journal={IEEE Transactions on Cloud Computing (TCC)},<br>
year=2014,<br>
month = Mar,<br>
volume = 2,<br>
number = 1,<br>
abstract={<br>
Data centers consume tremendous amounts of energy in<br>
terms of power distribution and cooling. Dynamic capacity<br>
provisioning is a promising approach for reducing energy<br>
consumption by dynamically adjusting the number of active<br>
machines to match resource demands. However, despite<br>
extensive studies of the problem, existing solutions have<br>
not fully considered the heterogeneity of both workload<br>
and machine hardware found in production environments. In<br>
particular, production data centers often comprise<br>
heterogeneous machines with different capacities and<br>
energy consumption characteristics. Meanwhile, the<br>
production cloud workloads typically consist of diverse<br>
applications with different priorities, performance and<br>
resource requirements. Failure to consider the<br>
heterogeneity of both machines and workloads will lead to<br>
both sub-optimal energy-savings and long scheduling<br>
delays, due to incompatibility between workload<br>
requirements and the resources offered by the provisioned<br>
machines. To address this limitation, we present Harmony,<br>
a Heterogeneity-Aware dynamic capacity provisioning<br>
scheme for cloud data centers. Specifically, we first use<br>
the K-means clustering algorithm to divide workload into<br>
distinct task classes with similar characteristics in<br>
terms of resource and performance requirements. Then we<br>
present a technique that dynamically adjusting the number<br>
of machines to minimize total energy consumption and<br>
scheduling delay. Simulations using traces from a<br>
Google's compute cluster demonstrate Harmony can reduce<br>
energy by 28 percent compared to heterogeneity-oblivious<br>
solutions.},<br>
}<br>
</pre>

<pre>
@INPROCEEDINGS{clusterdata:Di2013a,<br>
title = {Optimization of cloud task processing with checkpoint-restart mechanism},<br>
author = {Di, Sheng and Robert, Yves and Vivien, Fr\'ed\'eric and<br>
Kondo, Derrick and Wang, Cho-Li and Cappello, Franck},<br>
booktitle = {25th International Conference on High Performance Computing,<br>
Networking, Storage and Analysis (SC)},<br>
year = 2013,<br>
month = Nov,<br>
address = {Denver, CO, USA},<br>
abstract = {In this paper, we aim at optimizing fault-tolerance<br>
techniques based on a checkpointing/restart mechanism, in the<br>
context of cloud computing. Our contribution is<br>
three-fold. (1) We derive a fresh formula to compute the<br>
optimal number of checkpoints for cloud jobs with varied<br>
distributions of failure events. Our analysis is not only<br>
generic with no assumption on failure probability<br>
distribution, but also attractively simple to apply in<br>
practice. (2) We design an adaptive algorithm to optimize the<br>
impact of checkpointing regarding various costs like<br>
checkpointing/restart overhead. (3) We evaluate our optimized<br>
solution in a real cluster environment with hundreds of<br>
virtual machines and Berkeley Lab Checkpoint/Restart<br>
tool. Task failure events are emulated via a production trace<br>
produced on a large-scale Google data center. Experiments<br>
confirm that our solution is fairly suitable for Google<br>
systems. Our optimized formula outperforms Young's formula by<br>
3--10 percent, reducing wallclock lengths by 50--100 seconds<br>
per job on average.},<br>
}<br>
</pre>

<pre>
@inproceedings{clusterdata:Qiang2013-anomaly,<br>
author={Qiang Guan and Song Fu},<br>
title={Adaptive Anomaly Identification by Exploring Metric Subspace in Cloud Computing Infrastructures},<br>
booktitle={32nd IEEE Symposium on Reliable Distributed Systems (SRDS)},<br>
year=2013,<br>
month=Sep,<br>
pages={205--214},<br>
address={Braga, Portugal},<br>
abstract={ Cloud computing has become increasingly popular by<br>
obviating the need for users to own and maintain complex<br>
computing infrastructures. However, due to their inherent<br>
complexity and large scale, production cloud computing systems<br>
are prone to various runtime problems caused by hardware and<br>
software faults and environmental factors. Autonomic anomaly<br>
detection is a crucial technique for understanding emergent,<br>
cloud-wide phenomena and self-managing cloud resources for<br>
system-level dependability assurance. To detect anomalous<br>
cloud behaviors, we need to monitor the cloud execution and<br>
collect runtime cloud performance data. These data consist of<br>
values of performance metrics for different types of failures,<br>
which display different correlations with the performance<br>
metrics. In this paper, we present an adaptive anomaly<br>
identification mechanism that explores the most relevant<br>
principal components of different failure types in cloud<br>
computing infrastructures. It integrates the cloud performance<br>
metric analysis with filtering techniques to achieve<br>
automated, efficient, and accurate anomaly identification. The<br>
proposed mechanism adapts itself by recursively learning from<br>
the newly verified detection results to refine future<br>
detections. We have implemented a prototype of the anomaly<br>
identification system and conducted experiments in an<br>
on-campus cloud computing environment and by using the Google<br>
data center traces. Our experimental results show that our<br>
mechanism can achieve more efficient and accurate anomaly<br>
detection than other existing schemes.},<br>
}<br>
</pre>

<pre>
@ARTICLE{clusterdata:Zhani2013-HARMONY,<br>
title={{HARMONY}: dynamic heterogeneity-aware resource provisioning in the cloud},<br>
author={Qi Zhang and Mohamed Faten Zhani and Raouf Boutaba and<br>
Joseph L. Hellerstein},<br>
journal={The 33rd International Conference on Distributed Computing Systems (ICDCS)},<br>
year=2013,<br>
pages={510--519},<br>
month=Jul,<br>
address={Philadelphia, PA, USA},<br>
abstract={<br>
Data centers today consume tremendous amount of energy in<br>
terms of power distribution and cooling. Dynamic capacity<br>
provisioning is a promising approach for reducing energy<br>
consumption by dynamically adjusting the number of active<br>
machines to match resource demands. However, despite<br>
extensive studies of the problem, existing solutions for<br>
dynamic capacity provisioning have not fully considered<br>
the heterogeneity of both workload and machine hardware<br>
found in production environments. In particular,<br>
production data centers often comprise several<br>
generations of machines with different capacities,<br>
capabilities and energy consumption<br>
characteristics. Meanwhile, the workloads running in<br>
these data centers typically consist of a wide variety of<br>
applications with different priorities, performance<br>
objectives and resource requirements. Failure to consider<br>
heterogenous characteristics will lead to both<br>
sub-optimal energy-savings and long scheduling delays,<br>
due to incompatibility between workload requirements and<br>
the resources offered by the provisioned machines. To<br>
address this limitation, in this paper we present<br>
HARMONY, a Heterogeneity-Aware Resource Management System<br>
for dynamic capacity provisioning in cloud computing<br>
environments. Specifically, we first use the K-means<br>
clustering algorithm to divide the workload into distinct<br>
task classes with similar characteristics in terms of<br>
resource and performance requirements. Then we present a<br>
novel technique for dynamically adjusting the number of<br>
machines of each type to minimize total energy<br>
consumption and performance penalty in terms of<br>
scheduling delay. Through simulations using real traces<br>
from Google's compute clusters, we found that our<br>
approach can improve data center energy efficiency by up<br>
to 28\% compared to heterogeneity-oblivious solutions.},<br>
}<br>
</pre>

<pre>
@INPROCEEDINGS{clusterdata:Amoretti2013<br>
title = {A cooperative approach for distributed task execution in autonomic clouds},<br>
author = {Amoretti, M. and Lafuente, A.L. and Sebastio, S.},<br>
booktitle = {21st Euromicro International Conference on Parallel, Distributed<br>
and Network-Based Processing (PDP)},<br>
publisher = {IEEE},<br>
year = 2013,<br>
month = Feb,<br>
pages = {274--281},<br>
abstract = {Virtualization and distributed computing are two key<br>
pillars that guarantee scalability of applications deployed in<br>
the Cloud. In Autonomous Cooperative Cloud-based Platforms,<br>
autonomous computing nodes cooperate to offer a PaaS Cloud for<br>
the deployment of user applications. Each node must allocate<br>
the necessary resources for applications to be executed with<br>
certain QoS guarantees. If the QoS of an application cannot be<br>
guaranteed a node has mainly two options: to allocate more<br>
resources (if it is possible) or to rely on the collaboration<br>
of other nodes. Making a decision is not trivial since it<br>
involves many factors (e.g. the cost of setting up virtual<br>
machines, migrating applications, discovering<br>
collaborators). In this paper we present a model of such<br>
scenarios and experimental results validating the convenience<br>
of cooperative strategies over selfish ones, where nodes do<br>
not help each other. We describe the architecture of the<br>
platform of autonomous clouds and the main features of the<br>
model, which has been implemented and evaluated in the DEUS<br>
discrete-event simulator. From the experimental evaluation,<br>
based on workload data from the Google Cloud Backend, we can<br>
conclude that (modulo our assumptions and simplifications) the<br>
performance of a volunteer cloud can be compared to that of a<br>
Google Cluster.},<br>
doi = {10.1109/PDP.2013.47},<br>
ISSN = {1066-6192},<br>
address = {Belfast, UK},<br>
url = {http://doi.ieeecomputersociety.org/10.1109/PDP.2013.47},<br>
}<br>
</pre>

<pre>
@INPROCEEDINGS{clusterdata:Di2012b,<br>
title = {Host load prediction in a {Google} compute cloud with a {Bayesian} model},<br>
author = {Di, Sheng and Kondo, Derrick and Cirne, Walfredo},<br>
booktitle = {International Conference on High Performance Computing,<br>
Networking, Storage and Analysis (SC)},<br>
year = 2012,<br>
month = Nov,<br>
isbn = {978-1-4673-0804-5},<br>
address = {Salt Lake City, UT, USA},<br>
pages = {21:1--21:11},<br>
abstract = {Prediction of host load in Cloud systems is critical for<br>
achieving service-level agreements. However, accurate<br>
prediction of host load in Clouds is extremely challenging<br>
because it fluctuates drastically at small timescales. We<br>
design a prediction method based on Bayes model to predict the<br>
mean load over a long-term time interval, as well as the mean<br>
load in consecutive future time intervals. We identify novel<br>
predictive features of host load that capture the expectation,<br>
predictability, trends and patterns of host load. We also<br>
determine the most effective combinations of these features<br>
for prediction. We evaluate our method using a detailed<br>
one-month trace of a Google data center with thousands of<br>
machines. Experiments show that the Bayes method achieves high<br>
accuracy with a mean squared error of 0.0014. Moreover, the<br>
Bayes method improves the load prediction accuracy by 5.6--50\%<br>
compared to other state-of-the-art methods based on moving<br>
averages, auto-regression, and/or noise filters.},<br>
url = {http://dl.acm.org/citation.cfm?id=2388996.2389025},<br>
publisher = {IEEE Computer Society Press},<br>
}<br>
</pre>

<pre>
@INPROCEEDINGS{clusterdata:Zhang2012,<br>
title = {Dynamic energy-aware capacity provisioning for cloud computing environments},<br>
author = {Zhang, Qi and Zhani, Mohamed Faten and Zhang, Shuo and<br>
Zhu, Quanyan and Boutaba, Raouf and Hellerstein, Joseph L.},<br>
booktitle = {9th ACM International Conference on Autonomic Computing (ICAC)},<br>
year = 2012,<br>
month = Sep,<br>
isbn = {978-1-4503-1520-3},<br>
address = {San Jose, CA, USA},<br>
pages = {145--154},<br>
acmid = {2371562},<br>
publisher = {ACM},<br>
doi = {10.1145/2371536.2371562},<br>
keywords = {cloud computing, energy management, model predictive control,<br>
resource management},<br>
abstract = {Data centers have recently gained significant popularity<br>
as a cost-effective platform for hosting large-scale service<br>
applications. While large data centers enjoy economies of scale<br>
by amortizing initial capital investment over large number of<br>
machines, they also incur tremendous energy cost in terms<br>
of power distribution and cooling. An effective approach for<br>
saving energy in data centers is to adjust dynamically the<br>
data center capacity by turning off unused machines. However,<br>
this dynamic capacity provisioning problem is known<br>
to be challenging as it requires a careful understanding of the<br>
resource demand characteristics as well as considerations to<br>
various cost factors, including task scheduling delay, machine<br>
reconfiguration cost and electricity price fluctuation.<br>
In this paper, we provide a control-theoretic solution to<br>
the dynamic capacity provisioning problem that minimizes<br>
the total energy cost while meeting the performance objective<br>
in terms of task scheduling delay. Specifically, we model<br>
this problem as a constrained discrete-time optimal control<br>
problem, and use Model Predictive Control (MPC) to find<br>
the optimal control policy. Through extensive analysis and<br>
simulation using real workload traces from Google's compute<br>
clusters, we show that our proposed framework can achieve<br>
significant reduction in energy cost, while maintaining an<br>
acceptable average scheduling delay for individual tasks.},<br>
}<br>
</pre>

<pre>
@INPROCEEDINGS{clusterdata:Ali-Eldin2012<br>
title = {Efficient provisioning of bursty scientific workloads on the<br>
cloud using adaptive elasticity control},<br>
author = {Ahmed Ali-Eldin and Maria Kihl and Johan Tordsson and Erik Elmroth},<br>
booktitle = {3rd Workshop on Scientific Cloud Computing (ScienceCloud)},<br>
year = 2012,<br>
month = Jun,<br>
address = {Delft, The Nederlands},<br>
isbn = {978-1-4503-1340-7},<br>
pages = {31--40},<br>
url = {http://dl.acm.org/citation.cfm?id=2287044},<br>
doi = {10.1145/2287036.2287044},<br>
publisher = {ACM},<br>
abstract = {Elasticity is the ability of a cloud infrastructure to<br>
dynamically change the amount of resources allocated to a<br>
running service as load changes. We build an autonomous<br>
elasticity controller that changes the number of virtual<br>
machines allocated to a service based on both monitored load<br>
changes and predictions of future load. The cloud<br>
infrastructure is modeled as a G/G/N queue. This model is used<br>
to construct a hybrid reactive-adaptive controller that<br>
quickly reacts to sudden load changes, prevents premature<br>
release of resources, takes into account the heterogeneity of<br>
the workload, and avoids oscillations. Using simulations with<br>
Web and cluster workload traces, we show that our proposed<br>
controller lowers the number of delayed requests by a factor<br>
of 70 for the Web traces and 3 for the cluster traces when<br>
compared to a reactive controller. Our controller also<br>
decreases the average number of queued requests by a factor of<br>
3 for both traces, and reduces oscillations by a factor of 7<br>
for the Web traces and 3 for the cluster traces. This comes at<br>
the expense of between 20\% and 30\% over-provisioning, as<br>
compared to a few percent for the reactive controller.},<br>
}<br>
</pre>

<pre>
@INPROCEEDINGS{clusterdata:Sharma2011,<br>
title = {Modeling and synthesizing task placement constraints in<br>
{Google} compute clusters},<br>
author = {Sharma, Bikash and Chudnovsky, Victor and Hellerstein, Joseph L. and<br>
Rifaat, Rasekh and Das, Chita R.},<br>
booktitle = {2nd ACM Symposium on Cloud Computing (SoCC)},<br>
year = 2011,<br>
month = Oct,<br>
isbn = {978-1-4503-0976-9},<br>
address = {Cascais, Portugal},<br>
pages = {3:1--3:14},<br>
url = {http://doi.acm.org/10.1145/2038916.2038919},<br>
doi = {10.1145/2038916.2038919},<br>
publisher = {ACM},<br>
keywords = {benchmarking, benchmarks, metrics, modeling, performance<br>
evaluation, workload characterization},<br>
abstract = {Evaluating the performance of large compute clusters<br>
requires benchmarks with representative workloads. At Google,<br>
performance benchmarks are used to obtain performance metrics<br>
such as task scheduling delays and machine resource<br>
utilizations to assess changes in application codes, machine<br>
configurations, and scheduling algorithms. Existing approaches<br>
to workload characterization for high performance computing<br>
and grids focus on task resource requirements for CPU, memory,<br>
disk, I/O, network, etc. Such resource requirements address<br>
how much resource is consumed by a task. However, in addition<br>
to resource requirements, Google workloads commonly include<br>
task placement constraints that determine which machine<br>
resources are consumed by tasks. Task placement constraints<br>
arise because of task dependencies such as those related to<br>
hardware architecture and kernel version.<br>
<br>
This paper develops methodologies for incorporating task<br>
placement constraints and machine properties into performance<br>
benchmarks of large compute clusters. Our studies of Google<br>
compute clusters show that constraints increase average task<br>
scheduling delays by a factor of 2 to 6, which often results<br>
in tens of minutes of additional task wait time. To understand<br>
why, we extend the concept of resource utilization to include<br>
constraints by introducing a new metric, the Utilization<br>
Multiplier (UM). UM is the ratio of the resource utilization<br>
seen by tasks with a constraint to the average utilization of<br>
the resource. UM provides a simple model of the performance<br>
impact of constraints in that task scheduling delays increase<br>
with UM. Last, we describe how to synthesize representative<br>
task constraints and machine properties, and how to<br>
incorporate this synthesis into existing performance<br>
benchmarks. Using synthetic task constraints and machine<br>
properties generated by our methodology, we accurately<br>
reproduce performance metrics for benchmarks of Google compute<br>
clusters with a discrepancy of only 13\% in task scheduling<br>
delay and 5\% in resource utilization.},<br>
}<br>
</pre>

<pre>
@INPROCEEDINGS{clusterdata:Wang2011,<br>
title = {Towards synthesizing realistic workload traces for studying the<br>
{Hadoop} ecosystem},<br>
author = {Wang, Guanying and Butt, Ali R. and Monti, Henry and Gupta, Karan},<br>
booktitle = {19th IEEE Annual International Symposium on Modelling, Analysis,<br>
and Simulation of Computer and Telecommunication Systems (MASCOTS)},<br>
year = 2011,<br>
month = Jul,<br>
isbn = {978-0-7695-4430-4},<br>
pages = {400--408},<br>
url = {http://people.cs.vt.edu/~butta/docs/mascots11-hadooptrace.pdf},<br>
doi = {10.1109/MASCOTS.2011.59},<br>
publisher = {IEEE Computer Society},<br>
address = {Raffles Hotel, Singapore},<br>
keywords = {Cloud computing, Performance analysis, Design<br>
optimization, Software performance modeling},<br>
abstract = {Designing cloud computing setups is a challenging<br>
task. It involves understanding the impact of a plethora of<br>
parameters ranging from cluster configuration, partitioning,<br>
networking characteristics, and the targeted applications'<br>
behavior. The design space, and the scale of the clusters,<br>
make it cumbersome and error-prone to test different cluster<br>
configurations using real setups. Thus, the community is<br>
increasingly relying on simulations and models of cloud setups<br>
to infer system behavior and the impact of design choices. The<br>
accuracy of the results from such approaches depends on the<br>
accuracy and realistic nature of the workload traces<br>
employed. Unfortunately, few cloud workload traces are<br>
available (in the public domain). In this paper, we present<br>
the key steps towards analyzing the traces that have been made<br>
public, e.g., from Google, and inferring lessons that can be<br>
used to design realistic cloud workloads as well as enable<br>
thorough quantitative studies of Hadoop design. Moreover, we<br>
leverage the lessons learned from the traces to undertake two<br>
case studies: (i) Evaluating Hadoop job schedulers, and (ii)<br>
Quantifying the impact of shared storage on Hadoop system<br>
performance.}<br>
}<br>
</pre>