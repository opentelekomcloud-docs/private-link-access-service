:original_name: en-us_topic_0092087646.html

.. _en-us_topic_0092087646:

Do I Get an Active/Active or an Active/Passive Architecture?
============================================================

We always require two links to Open Telekom Cloud (only exception: PLAS Ethernet Light, which requires only one WAN link). For all other PLAS Ethernet options and PLAS Cloud Exchange, you need to connect two independent links by yourself. With PLAS MPLS, this is done automatically between your network provider and PLAS. You order one cloud link from your network provider as part of your contract, but technically they use two redundant links to Open Telekom Cloud.

Even if you always have two physical and logical links to PLAS, you only can use one IP link on top of them. The second link is always the redundant link and passive for backup cases. This means that you cannot use both links for features such as link aggregation or load balancing.
