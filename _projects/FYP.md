---
title: "Air Pollution based Routing Algorithm for VANETs"
collection: projects
type: "Project"
permalink: /projects/FYP
venue: "National Conference on Information and Communication Technologies (NCICT)"
date: 2020-02-15
location: "Chennai, India"

---

## Abstract

Vehicular Ad-Hoc Network (VANET) is a type of network that is created from the concept of establishing a network of cars for a specific need or situation. VANETs have
now been established as reliable networks that vehicles use for communication purpose on highways or urban environments. The two most important aspects of VANETs are Vehicle to
Vehicle communication (V2V) and Vehicle to Infrastructure communication (V2I), they form an important part of the Intelligent Transport Systems (ITS) architecture. With the
travelling time being given more priority for routing, often the emissions and the air pollution data is not included. With the
rising pollution and an increase in the volume of vehicles and traffic, it is necessary to devise a system where these parameters
are taken into account. The objective of the work is to provide a route with minimal pollution using an air pollution based routing algorithm. The proposed algorithm identifies the Air
Quality Index (AQI) of the streets and provides the route with the lowest mean AQI to the vehicle. The algorithm was
simulated on a realistic map of a region of Chennai with vehicular traffic using OMNeT++ and SUMO as a VANET
network simulator with Veins framework. The performance of the algorithm was analyzed by monitoring the parameters like mean AQI, total travel time and the distance travelled by the
vehicle for a specific set of ten vehicles throughout their journey from its source to the destination location.

## Simulation Scenario

In order to perform and obtain realistic and reliable results for evaluation, this work uses realistic traffic and map
data for the simulation. For the traffic demand and network of roads and streets, a data set of a part of Chennai consisting of
Kodambakkam, Choolaimedu and Nungambakkam was obtained from OpenStreetMap (OSM) and has been used for a realistic simulation.

<p align="center">
  <img src="https://marjerie.github.io/files/osm.jpg?raw=true" alt="Photo" style="width: 450px;"/> 
</p>

In the project, SUMO (traffic simulator) along withOMNeT++, integrated using Veins framework, is employed to simulate the air pollution based routing using A* search
algorithm. It is investigated in the ideal form, that is, without any wireless communications technique to properly analyze the efficacy of the algorithm alone. In
order to investigate the effect of the algorithm and its effect on the route changing, initially, a set of vehicles are simulated to mimic realistic traffic in the area and then, 10 vehicles are
released from different sources, one by one, with each vehicle having its own destination. They were monitored until all the 10 vehicles reached its specified destination.

<p align="center">
  <img src="https://marjerie.github.io/files/sim.jpg?raw=true" alt="Photo" style="width: 450px;"/> 
</p>

To figure out the effect of the A* search algorithm based routing using the AQI of the different streets, two different
simulations were done as follows:
1. First, the 10 vehicles were given fixed routes initially which were obtained using the travel time as cost. At no point in the simulation were the routes changed in this case.
2. In the second simulation, the 10 vehicles were given
routes based on the A* algorithm which used the AQI of the streets as the cost. Here, the routes were allowed to change dynamically based on the AQI of the route throughout
the course of the simulation. The changing route for all the vehicles were constantly recorded for analysis.

## Results 

**Mean Air Quality Index (AQI)**

It can be seen that in all of the cases the new route has a lower mean AQI. An average reduction of 18 units in mean AQI is observed. 

<p align="center">
  <img src="https://marjerie.github.io/files/aqigraph.jpg?raw=true" alt="Photo" style="width: 450px;"/> 
</p>

**Distance Travelled**

The values of distance travelled with and without using the algorithm are almost the same. These results are seen as acceptable as the
absolute difference between the two values is very less and
is hence considered as negligible.

<p align="center">
  <img src="https://marjerie.github.io/files/distgraph.jpg?raw=true" alt="Photo" style="width: 450px;"/> 
</p>

**Total Travel Time**

It can be inferred that there is mostly a very small increase and occasionally a decrease in the total travel time when compared the case where the algorithm is
not used. This increase can be considered as an acceptable trade-off as the increase in travel time results in a very good decrease in the mean AQI as observed in the vehicle 5.

<p align="center">
  <img src="https://marjerie.github.io/files/ttgraph.jpg?raw=true" alt="Photo" style="width: 450px;"/> 
</p>
