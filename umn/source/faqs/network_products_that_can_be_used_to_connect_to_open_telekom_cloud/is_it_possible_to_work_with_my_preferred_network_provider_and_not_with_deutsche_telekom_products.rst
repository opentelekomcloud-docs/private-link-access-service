:original_name: en-us_topic_0092087644.html

.. _en-us_topic_0092087644:

Is It Possible to Work with my Preferred Network Provider and Not with Deutsche Telekom Products?
=================================================================================================

First, you should check the option of using Equinix Cloud Exchange. In this case, your provider can establish the connection to an Equinix location with ECX as needed.

There is currently no option to connect a third-party MPLS network directly to Open Telekom Cloud. We are open to providers connecting their platforms to Open Telekom Cloud. To do so, they need to establish redundant links to our data centers in Biere and Magdeburg with 10 Gbit/s as a minimum requirement. In addition, they need to create interfaces based on our Open Telekom Cloud API set for private links.

If you need an Ethernet or Lambda line which is terminated in the Open Telekom Cloud, we only support 10 Gbit/s redundant lines to Biere/Magdeburg. In this case, the network provider is responsible for offering access to the PLAS ports we offer. Since there will be no contract between the network provider and Open Telekom Cloud, the customers themselves will have to take care of project management and are responsible for their connectivity to the Open Telekom Cloud edge routers.
