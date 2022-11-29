:original_name: en-us_topic_0092087627.html

.. _en-us_topic_0092087627:

What is PLAS Ethernet Light?
============================

PLAS Ethernet Light is a combination of PLAS Ethernet Redundant and Ethernet Connect.

The difference to PLAS Ethernet Redundant is that there is only one Ethernet Connect link on the network side.

Behind the termination point of the link, Open Telekom Cloud uses two uplinks to two different PLAS ports and routes them to different AZs where your VPC is hosted.

This means that you do not have any (private) backup on the line and your production might have to stop if the link is required.

For this reason, we do not recommend this option, but offer it to leave the choice to you.

For more information on Ethernet Connect, see chapter "Network products that can be used to connect to Open Telekom Cloud" or see the Network section on the Deutsche Telekom website for "`Geschäftskunden <https://geschaeftskunden.telekom.de/vernetzung-digitalisierung/vernetzung/standortvernetzung>`__".
