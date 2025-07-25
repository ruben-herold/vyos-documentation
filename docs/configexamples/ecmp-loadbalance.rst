=====================================
VyOS aѕ ECMP router for loadbalancing
=====================================

Scenario and requirements
=========================

This example shows how to configure a VyOS as ECMP router for loadbalancing.

Diagram used in this example:

.. image:: /_static/images/VyOS-ECMP.png
    :width: 80%
    :align: center
    :alt: Network Topology Diagram

The diagram shows the complete stack. In this documentation we will focus on 
connecting the load balance to the routers. 

In this example we use extended nexthop to transport IPv4 over IPv6 (RF8950).

Prerequisites
============= 

- Two VyOS routers with uplink and ibgp 

- Three loadbalancer, in this example we use linux + nginx + exabgp

- A bunch of Webservers reachable from the loadbalancer

    
+---------------------------------------+---------------------+
| VyOS ASN                              |  65536              |
+---------------------------------------+---------------------+
| Loadbalancer ASN                      |  65537              |
+---------------------------------------+---------------------+
| Router ID VyOS A                      |  192.0.2.1          |
+---------------------------------------+---------------------+
| Router ID VyOS B                      |  192.0.2.2          |
+---------------------------------------+---------------------+
| Router ID LB01                        |  192.0.2.3          |
+---------------------------------------+---------------------+
| Router ID LB02                        |  192.0.2.4          |
+---------------------------------------+---------------------+
| Router ID LB03                        |  192.0.2.5          |
+---------------------------------------+---------------------+
| Network between VyOS and LB'S         |  2001:db8:1::/64    |
+---------------------------------------+---------------------+
| Service IPv4                          |  198.51.100.1       |
+---------------------------------------+---------------------+
| Service IPv6                          |  2001:db8::1/128    |
+---------------------------------------+---------------------+


Configuration VyOS
==================

VyOS A
-------

VyOS B
-------

Configuration LB
================

LB01
----

LB02
----

LB03
----




