:original_name: en-us_topic_0092087651.html

.. _en-us_topic_0092087651:

Can I Use PLAS as a Site-to-Site Network for my Subsidiaries and Data Centers?
==============================================================================

PLAS is only used to access your VPC on Open Telekom Cloud. It is not possible to use it as a routing instance to connect two or more locations. But if you are planning to use a virtual overlay network to support such connectivity architectures, you might work with virtual routers on top of your VMs and handle the existing connectivity on private and internet access for an overlay network. Please bear in mind that neither PLAS nor Direct Connect will monitor these activities and that you are fully responsible for the overlay network.
