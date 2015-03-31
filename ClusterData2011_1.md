_John Wilkes and Charles Reiss._<br>Copyright © 2011 Google Inc. All rights reserved.<br>
<br>
<table><thead><th><font color='red'><b>This trace is being deprecated in favor of <a href='ClusterData2011_2.md'>clusterdata-2011-2</a>, and will be deleted some time after 2014-12-18.</b></font></th></thead><tbody></tbody></table>

This document describes some properties of the trace we are releasing called <code>clusterdata-2011-1</code>.<br>
<br>
The trace represents 29 day's worth of cell information from May 2011, on a cluster of about 11k machines.  <b>To find out how to download it, and what it contains, read the TraceVersion2 of the trace data schema and format.</b>

The trace starts at 19:00 EDT on Sunday May 1, 2011, and the datacenter is in that timezone (US Eastern).  This corresponds to a trace timestamp of 600s; see the data schema documentation for why.<br>
<br>
<h1>Trace data</h1>

The trace is stored in <a href='https://developers.google.com/storage/'>Google Storage for Developers</a> in the bucket called <code>clusterdata-2011-1</code>.  Here's a link to the <a href='https://storage.cloud.google.com/?arg=clusterdata-2011-1'>web UI for that bucket</a>. Most users will want the <a href='https://developers.google.com/storage/docs/gsutil'>gsutil</a> command-line tool to download the trace data.<br>
<br>
The total size of the compressed trace is approximately 40GB.<br>
<br>
Priorities in this trace range from 0 to 11 inclusive; bigger numbers mean "more important". 0 and 1 are “free” priorities; 9, 10, and 11 and “production” priorities; and 10 is a “monitoring” priority.<br>
<br>
<h1>Known anomalies in the trace</h1>

Disk-time-fraction data is only included in about the first 14 days, because of a change in our monitoring system.<br>
<br>
Some jobs are deliberately omitted because they ran primarily on machines not included in this trace. The portion that ran on included machines amounts to approximately 0.003% of the machines’ task-seconds of usage.<br>
<br>
We are aware of only one example of a job that retains its job ID after being stopped, reconfigured, and restarted (job number 6253771429).<br>
<br>
Approximately 70 jobs (for example, job number 6377830001) have job event records but no task event records. We believe that  this is legitimate in a majority of cases: typically because the job is started but its tasks are disabled for its entire duration.<br>
<br>
Approximately 0.013% of task events and 0.0008% of job events in this trace have a non-empty missing info field.<br>
<br>
We estimate that less than 0.05% of job and task scheduling event records are missing and less than 1% of resource usage measurements are missing.<br>
<br>
Some cycles per instruction (CPI) and memory accesses per instruction (MAI) measurements are clearly inaccurate (for example, they are above or below the range possible on the underlying micro-architectures). We believe these measurements are caused by bugs in the data-capture system used, such as the cycle counter and instruction counter not being read at the same time. To obtain useful data from these measurements, we suggest filtering out measurements representing a very small amount of CPU time and measurements with unreasonable CPI and MAI values.<br>
<br>
<h1>Change log</h1>

<table><thead><th>2014-11-18 10:10</th><th> Replaced by <a href='ClusterData2011_2.md'>clusterdata-2011-2</a>. </th></thead><tbody>
<tr><td>2013.05.10 11:46</td><td> Changed Google Storage link; added bucket and gsutil pointers. </td></tr>
<tr><td>2012.12.29 12:36</td><td> Trace start time added.</td></tr>
<tr><td>2011.11.14 18:21</td><td> New data copied out. Please let us know if there any issues with it.</td></tr>
<tr><td>2011.11.14 10:10</td><td> The partial update had unexpected consequences (e.g., mismatched SHA256SUM entries); new data will be copied over today.</td></tr>
<tr><td>2011.11.13 00:07</td><td> The trace_events files are no longer missing machine_ids. Apologies for any inconvenience.</td></tr>
<tr><td>2011.11.08 23:30</td><td> Note: a small hiccup has been found: the trace_events file is missing the machine_ids.  It's being worked on now.</td></tr></tbody></table>

All tImes are from the Pacific time zone.