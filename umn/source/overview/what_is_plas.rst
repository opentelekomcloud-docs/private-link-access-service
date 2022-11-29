:original_name: en-us_topic_0218777868.html

.. _en-us_topic_0218777868:

What Is PLAS?
=============

Private link access service (PLAS) enables public cloud platform users to establish exclusive connections from their on-premise networks to VPCs on the public cloud platform.

PLAS connections are established between carrier networks and Direct Connect gateways, reducing network latency. These connections outperform Internet connections in stability and security.

PLAS supports manual provisioning and self-service provisioning.

-  Manual provisioning

   Manual provisioning helps to connect a Layer 2 private network (EC) to a VPC on the open telekom cloud (OTC). EC is an acronym for the Ethernet Connect.

   When network links are ready, configure PLAS links and cloud private lines in a template and send the edited template to sales personnel.

-  Self-service provisioning

   Self-service provisioning helps to connect a Layer 3 private network (IP VPN) to a VPC on the OTC.

   After a PLAS connector is created, a VPN link is automatically generated between the edge gateway and cloud gateway on the IP VPN. This link supports high-speed, exclusive, and reliable transmission of services and data.

   PLAS connectors can only connect IPLS (IntraSelect MPLS) private lines to the OTC.


.. figure:: /_static/images/en-us_image_0249207722.png
   :alt: **Figure 1** PLAS connector introduction

   **Figure 1** PLAS connector introduction

.. note::

   -  PCNE: PLAS connector network edge
   -  PCCE: PLAS connector cloud edge
