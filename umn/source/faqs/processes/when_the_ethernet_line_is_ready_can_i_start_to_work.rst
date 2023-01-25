:original_name: en-us_topic_0092087661.html

.. _en-us_topic_0092087661:

When the Ethernet Line Is Ready, Can I Start to Work?
=====================================================

Connecting your company via Ethernet (layer 2 service) means that there are two connectivity layers to deploy. The first layer is layer 2 connectivity, which is set up in collaboration between the network provider and Open Telekom Cloud/PLAS.

In addition to the layer 2 connection, an eBGP protocol must be established between the PLAS router and the customer's edge router and/or firewall (see in the category "Processes": "Do customers have to set up eBGP themselves?")

Finally, on top of this router-to-router connectivity, you need to establish communication between your local network with private IP addresses and your Open Telekom Cloud environment, which also runs with your private addresses under your own responsibility. In summary, you need to take care of addresses, firewalls, security groups and routing between the instances.

Work can only start once all three parts are ready and functional.
