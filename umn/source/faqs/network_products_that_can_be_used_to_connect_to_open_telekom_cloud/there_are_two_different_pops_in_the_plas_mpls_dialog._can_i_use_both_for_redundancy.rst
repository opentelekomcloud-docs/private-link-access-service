:original_name: en-us_topic_0092087642.html

.. _en-us_topic_0092087642:

There Are Two Different POPs in the PLAS MPLS Dialog. Can I Use Both for Redundancy?
====================================================================================

PLAS allows one VPN per subnet. Direct Connect creates that VPN and is based on a redundant link to one MPLS-POP. You only can choose whether the POP is in location A or location B. Please ask your network provider to learn more about the best choice.

If you need higher redundancy, you need to create another subnet with a second Direct Connect on Open Telekom Cloud and a second Cloud Connect Link on MPLS. Now you have four links, i.e. two active and two passive links.

You have to take care of the routing logic by yourself. Open Telekom Cloud sees both links as independent and cannot decide where traffic will flow.
