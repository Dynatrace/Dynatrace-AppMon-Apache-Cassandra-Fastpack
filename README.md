<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>Apache Cassandra Fastpack</title>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8"/>
<meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
<meta content="Scroll Wiki Publisher" name="generator"/>
<link type="text/css" rel="stylesheet" href="css/blueprint/liquid.css" media="screen, projection"/>
<link type="text/css" rel="stylesheet" href="css/blueprint/print.css" media="print"/>
<!--[if lt IE 8]><link rel="stylesheet" href="css/blueprint/ie.css" type="text/css" media="screen, projection"/><![endif]-->
<link type="text/css" rel="stylesheet" href="css/content-style.css" media="screen, projection, print"/>
<link type="text/css" rel="stylesheet" href="css/screen.css" media="screen, projection"/>
<link type="text/css" rel="stylesheet" href="css/print.css" media="print"/>
</head>
<body>
<div class="container" style="min-width: 760px;">
<div class="header block">
<div class="header-left column span-6">
</div>
<div class="column span-18 header-right last">
<h4>Apache Cassandra Fastpack</h4>
</div>
</div>
<div class="block">
<div class="toc column span-6 prepend-top">
<h3>Table of Contents
</h3>
<ul class="toc">
</ul>
</div>
<div id="65732667" class="content column span-18 last">
<h1>Apache Cassandra Fastpack</h1>
<div class="section-2" id="65732667_ApacheCassandraFastpack-Overview" >
<h2>Overview</h2>
<p>
<img src="images_community/download/attachments/25789254/cassandra_logo_small.png" alt="images_community/download/attachments/25789254/cassandra_logo_small.png" class="confluence-embedded-image image-left" />
</p>
<p>
</p>
<p>
The dynaTrace FastPack for the Apache Cassandra NoSQL Database enables easy out-of-the-box monitoring. The FastPack consists predefined JMX Measures for Cassandra, Sensors for Cassandra Server and Cassandra Clients, Business Transactions a Template Profile and Dashboards. </p>
</div>
<div class="section-2" id="65732667_ApacheCassandraFastpack-FastPackDetails" >
<h2>Fast Pack Details</h2>
<div class="tablewrap">
<table>
<thead class=" "></thead><tfoot class=" "></tfoot><tbody class=" "> <tr>
<td rowspan="1" colspan="1">
<p>
Name </p>
</td>
<td rowspan="1" colspan="1">
<p>
<strong class=" ">Apache Cassandra Monitoring FastPack</strong> </p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>
Version </p>
</td>
<td rowspan="1" colspan="1">
<p>
1.0.0 </p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>
dynaTrace Version </p>
</td>
<td rowspan="1" colspan="1">
<p>
4 </p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>
Author </p>
</td>
<td rowspan="1" colspan="1">
<p>
Michael Kopp </p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>
License </p>
</td>
<td rowspan="1" colspan="1">
<p>
<a href="attachments_5275722_2_dynaTraceBSD.txt">dynaTrace BSD</a> </p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>
Support </p>
</td>
<td rowspan="1" colspan="1">
<p>
<a href="https://community/display/DL/Support+Levels#SupportLevels-Community">Not Supported </a> </p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>
FastPack Contents </p>
</td>
<td rowspan="1" colspan="1">
<p>
<a href="attachments_65962002_2_dynaTrace_Cassandra_FastPack.dtp">Fastpack Download</a> contains: </p>
<ul class=" "><li class=" "> <p>
Cassandra Performance Overview </p>
</li><li class=" "> <p>
Template Profile </p>
<ul class=" "><li class=" "> <p>
Server and Client Sensors </p>
</li><li class=" "> <p>
Business Transactions for Cassandra Server and Client Actions </p>
</li><li class=" "> <p>
Business Transaction to monitor Compaction (Versions 0.8,1.x) </p>
</li></ul></li></ul> </td>
</tr>
<tr>
<td rowspan="1" colspan="1">
</td>
<td rowspan="1" colspan="1">
</td>
</tr>
</tbody> </table>
</div>
</div>
<div class="section-2" id="65732667_ApacheCassandraFastpack-CassandraPerformanceOverview" >
<h2>Cassandra Performance Overview</h2>
<p>
<img src="images_community/download/attachments/65732667/Cassandra_Dashboard.png" alt="images_community/download/attachments/65732667/Cassandra_Dashboard.png" class="" />
</p>
<p>
The Cassandra Load Dashboard gives an Overview of Client and Server Side performance and Load. </p>
<ul class=" "><li class=" "> <p>
Client Side Times (avg/max)<br/>This first row shows the Cassandra response time from the applications point of view. It automatically splits into its separate operation types and shows average and max for each. this can be used to see if there is a big difference between server and client performance and if the response time is volatile </p>
</li><li class=" "> <p>
Server Side Load<br/>This shows the number of requests per operation types that are executed on the Cassandra servers </p>
</li><li class=" "> <p>
Server Side Response Times (avg/max)<br/>Shows the Cassandra server side response time per operation type. It shows average and max to give a feeling of volatility </p>
</li><li class=" "> <p>
Cassandra CPU Load<br/>This show the average CPU load over all Cassandra instances </p>
</li><li class=" "> <p>
Active and Pending Tasks<br/>Cassandra executes several tasks per request and other background tasks. Under normal circumstances there should be no backlog. Once an instance starts to get overloaded in some area the active and subsequently the pending tasks will be rising. If this shows a continuous growing trend you need to investigate further. If it is stable but none zero there is room to optimize </p>
</li><li class=" "> <p>
GC Suspensions and Cassandra Compactions<br/>Cassandra is sensitive to Garbage Collection. Frequent GC suspensions indicate too much load and or non optimal configuration of the memtables.<br/>Cassandra also needs to do Compaction on its data. If this happens too often or takes too long the it is either overloaded or the memtables are not configured correctly for one of the column families. </p>
</li></ul> </div>
<div class="section-2" id="65732667_ApacheCassandraFastpack-BusinessTransactions" >
<h2>Business Transactions</h2>
<ul class=" "><li class=" "> <p>
Cassandra Compaction<br/>There are two versions of this Business Transaction, one for the current 1.0.x release and one for the last stable release (0.8.x). The newer one shows compaction per keyspace and column family. The older one shows compaction per column family and SSTable. </p>
</li><li class=" "> <p>
Cassandra Action<br/>Shows Cassandra Server Side Operations. Those include the typical get, get_slice, batch_mutate and others </p>
</li><li class=" "> <p>
Cassandra Client<br/>Shows Cassandra Client Side Operations. Those include the typical get, get_slice, batch_mutate and others </p>
</li></ul> </div>
<div class="section-2" id="65732667_ApacheCassandraFastpack-FastPackInformation" >
<h2>FastPack Information</h2>
<p>
The Fastpack contains a Dashboard and a Template System Profile. In addition it contains a Metric Group for Cassandra JMX Measures, some of which are already subscribed in the system profile.<br/>dynaTrace can monitor any JMX attribute available withing Cassandra in addition to those supplied in this fastpack.<br/>The System Profile already contains an Agent Group for Cassandra, just add the dynaTrace agent to your JVM_OPTS when starting Cassandra (use name=Cassandra). This agent group contains some minor modifications to allow optimal monitoring of Cassandra.<br/>The System profile also contains all necessary Sensors to monitor both Server and client side. Add the Cassandra Common Sensor group in your own agent groups. </p>
</div>
<div class="section-2" id="65732667_ApacheCassandraFastpack-Installation" >
<h2>Installation</h2>
<p>
Just download and import the FastPack on your dynaTrace Server (see <a href="https://community.compuwareapm.com/community/display/DOCDT40/Plugin+Management">Plugin Management</a>) </p>
<p>
If you start with a fresh system simply copy the provided System profile (to give it an application specific name) and add agent groups for your own application. If you want to use Cassandra in an existing System profile please copy the following items to your system profile. </p>
<ul class=" "><li class=" "> <p>
Cassandra Business Transactions (you only need to copy those that apply to your Cassandra version) </p>
</li><li class=" "> <p>
Both sensor groups </p>
</li><li class=" "> <p>
the Cassandra Agent Group cannot be copied please do the following </p>
<ul class=" "><li class=" "> <p>
Create a separate agent group for Cassandra </p>
</li><li class=" "> <p>
apply both Cassandra sensor groups </p>
</li><li class=" "> <p>
disable the Executor Tagging sensor </p>
</li></ul></li></ul> </div>
</div>
</div>
<div class="footer">
</div>
</div>
</body>
</html>
