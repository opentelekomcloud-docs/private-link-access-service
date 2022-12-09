:original_name: en-us_topic_0092087630.html

.. _en-us_topic_0092087630:

What Is PLAS Cloud Exchange? (aka PLAS CX)
==========================================

Many customers have existing architectures for accessing cloud environments via cloud exchange brokers or want to start using this solution. It is very flexible in case of multi-cloud strategies and enables customers to easily change connections or bandwidth. From the customers' perspective, it represents their "cloud connectivity hub."

Nearly all colocation providers have their own cloud connectivity broker. We decided to start with Equinix Cloud Exchange (ECX).

PLAS is connected to Equinix Cloud Exchange on the "seller side." Customers connect to ports on the "seller-side", and both meet on the portal. Here, customers can see the Open Telekom Cloud as well as many other clouds, and they can book and assign virtual circuits with different bandwidths to Open Telekom Cloud. You need to choose one link to the data center in Biere and one to the data center in Magdeburg, representing two of our AZs.

ECX and Open Telekom Cloud enable layer 2 connectivity. Please note that redundancy is only ensured when using this logic, since there is no line redundancy. Redundancy only works on the IP layer.

You can access the service directly from all ECX locations in Frankfurt and from all European ECX locations via the remote option of ECX. This means that your traffic will use the backbone of Equinix. While this is a paid service, it offers a flexible way to connect other cloud areas without building your own networks.

First, you need to establish Direct Connect and PLAS in your VPC. This requires you to enter some technical information in the dialog on the ECX portal.

It will take some days to establish the link between Open Telekom Cloud and ECX. In a second step, you need to establish the IP connectivity between your VPC and your local LAN.

You can access ECX from your local colocation cage at Equinix or via a network of your choice.

For more information on Equinix Cloud Exchange, please visit the `Equinix website <https://www.equinix.de/interconnection-services/cloud-exchange-fabric/>`__.
