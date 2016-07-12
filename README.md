[![Stories in Ready](https://badge.waffle.io/csae1152/MyPredictiveFarm.png?label=ready&title=Ready)](https://waffle.io/csae1152/MyPredictiveFarm)
[![Stories in Ready](https://badge.waffle.io/csae1152/MyPredictiveFarm.png?label=ready&title=Ready)](https://waffle.io/csae1152/MyPredictiveFarm)
Overview - What can we do for you...
====================================

With our platform you will be able to communicate with agricultural workers around the world helping you getting better in what you do.

You will be able to perform retinal image analysis by uploading an image from your cow's retina and see what diseas will or will not show up. 

Our solution is connected with all your farm devices, collecting all the produced information and will provide you strategies and plans for the future.

It will get possible to find the best solutions for your harvesting machines.

In combination with sensors around your acre, weather forecast and predictive analysis our platform will provide you with the information you need.

Technical Overview (First draft)
=====================================================

- Tomcat

- MySQL

- HAProxy

- Nginx

- Memcached

- EHCache

- Apache

- Elasticsearch

- Redis

- RabbitMQ

- CentOS

- Puppet

- New Relic

- AppDynamics

- ZooKeeper

- LDAP

- Nagios

- Graphite

- Cacti

- Apache FTP server

- OpenTSDB

- Google BigQuery

- Google BigTable

- Google analytics

- MixPanel

- Tableau

- ReactJS/Backbone/Marionette/JQuery/npm/nighwatch

- Rsync

- PowerDNS

- Mashery

- SOA architecture based on REST apis.

- Java used to power core file system code

- Native Android/iOS apps

- Desktop and server sync client for various platforms

- GCE

- GCS/S3/Azure

Retinal Image Analysis
======================

A big part of our application will be computer aided diagnosis for your animals.

It's easy as pie: 

- Take an image of your animals retina with your smart phone.
- Upload it to your MyPredectiveFarm retinal image analysis application
- Get the results in a few seconds
- You will see if your animals are in a good health condition or what diseas you will have to expect.

Technical overview of retinal image 
===================================
 

Try it out
==========

Please have a look at your first release: http://jbossvertx-easyfarming.rhcloud.com/

We are maintaining a blog to keep you up to date:  http://mypredectivefarm.blogspot.co.at/

Great! We are on Google+: https://plus.google.com/u/0/communities/118045655178910862948

MyPredectiveFarm uses a set of technologies that interact between them to implement these layers:

Apache Kafka: this is our data stream. Different devices will be generating messages in Kafka topics.

Schema registry - We will use Avro-schemas for Kafka topics.
REST proxy which will allow us to consume Kafka topics.
Camus, a Map-Reduce-Job to store messages from Kafka into HDFS.

HDFS: this is where our main dataset is stored.

MapReduce: This is how our batch layer recomputes batch views. Mapreduce is also used for a batch ETL process that dumps data from Kafka to HDFS.

Apache Storm: This is what we use as our speed layer. Events are consumed from Kafka and processed into “realtime views”

HBase: This is where we store the “realtime biddings” generated by Storm topologies (Publisher).

Upcoming Features
=================

 - Retina image upload via tracking.js
 - Rainfall forecast
 - Bidding platform for agricultural devices
 - Decision dashboards for buying devices
 
Predictive analysis
===================

With our predictive engine we will let you know what will happen in the future.
We will provide you easy to read predictive analysis charts. (Based on d3.js)

Overview - Technical layout of retinal image analysis
=====================================================

Prediction Network

An input vector sequence x = (x1, . . . , xT ) is passed through weighted connections to a stack of N recurrently connected hidden layers to compute first the hidden vector sequences h.

And then the output vector sequence y = (y1, . . . , yT ). Each output vector yt is used to
parameterise a predictive distribution Pr(xt+1|yt) over the possible next inputs
xt+1. The first element x1 of every input sequence is always a null vector whose
entries are all zero; the network therefore emits a prediction for x2, the first
real input, with no prior information. The network is ‘deep’ in both space
and time, in the sense that every piece of information passing either vertically
or horizontally through the computation graph will be acted on by multiple
successive weight matrices and nonlinearities.

copyright by http://arxiv.org/pdf/1308.0850v5.pdf - Alex Graves

Loos weight function for estimating edges in the picture.

Frontend architecture overview
==============================

We think react and redux/flux is a good thing. So we plan to use it.

- Browserify
- Babel(ES6)
- Handlebars
- Gulp
- Mocha + Chai
- Sinon
- Pioneer

and on top it's Backbone.js running.


 

