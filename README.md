# (Dynamic) Temporal Network Visualization 

As we know, sometimes a network might be not static. For instance, in a friendship network, a friendship connection between two people changes by time.
What I mean by that is, in a temporal network, some vertices may be connected but only at some particular point(s) of time. With that factor, 
we cannot simply use a static visualization for a temproal network. Instead, we create sequence of static visualizations in order to visualize 
a temporal network. For this purpose, in this project, I use `tsna` and `ndtv` packages to visualize and analyze a temporal network.

The main visualization will look like the following picture which can be played like a video (in the actual result).
To see the actual result, check [here](https://www.rpubs.com/Steven_Surya/Dynamic-network).

<img src="dynamic network.png" width="700" height="500">

One of the important feature for analyzing a temporal network is about temporal connectivity. In other words, whether or not vertices are connected
by temporal path(s). What I mean by that is, look at the picture above, when **t=0** (the starting timestamp), "Ridolfi" and "Tornabuoni" are disconnected.
Suppose that the connection in that picture represents a business connection between two people. We know that this kind of connection create a temporal 
network that changes over time. Suppose that we got a report that during **t=0** to **t=25**, Ridolfi collected massive amount of illegal money 
and in order to make it less obvious, he hid and distributed the money to some of his business partners and told them to keep the money for him in 
exchange to some percentage of it. To avoid suspicion, his business partners also distribute the money that they got in a similar manner to their
business partners (may not be a business partner of Rudolfi) and so on, indefinitely. The police want to know about whether or not it is possible that 
Tornabuoni also took a part in this scheme. If it is possible, then in what scenario Tornabuoni could be the part of this scheme?
We can observe this by knowing whether or not Rudolfi and Tornabuoni are temporal-connected in the network.

<img src="temporal path.png" width="900" height="500">

From the above visualization, it turns out that it is possible, since they're temporal-connected.
The possible scenario is, at **t=13**, Ridolfi shared the money to Sarbadori, then Sarbadori shared the money to Lamberteschi. 
This is possible, since they form business connections at **t=13**.
Then, at **t=21**, Lamberteschi shared the money to Tornabuoni, since they are business partners at **t=21**.

For more detail, check [here](https://www.rpubs.com/Steven_Surya/Dynamic-network)
