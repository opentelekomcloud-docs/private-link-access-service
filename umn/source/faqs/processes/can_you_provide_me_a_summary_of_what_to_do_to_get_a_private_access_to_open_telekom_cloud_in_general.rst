:original_name: en-us_topic_0092087660.html

.. _en-us_topic_0092087660:

Can You Provide Me a Summary of What to Do to Get a Private Access to Open Telekom Cloud in General?
====================================================================================================

-  Create an architecture including physical links, VPC structure, IP address scheme, security and redundancy model
-  Inform your internal IT department and your Open Telekom Cloud administrator to check and be prepared
-  Decide what WAN architecture you want to use and which provider you prefer
-  Ask your provider whether they are able to support you with access to Open Telekom Cloud
-  Now you have a plan
-  Agree a contract with your network provider and see how long they need for implementation
-  Depending on the duration for the network part, start with deploying Direct Connect in your VPC
-  Also create PLAS with your preferred option for ports and bandwidth
-  Inform your security and IT departments that they need to set up config for eBGP on edge router/firewall
-  Check that the firewalls in your local network are open for the IP address used (your address space)
-  When everything is ready: check your connectivity
-  If ok: great; if not: open a ticket to find out whether the failure is caused by your external network or Open Telekom Cloud
