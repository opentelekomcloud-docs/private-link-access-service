:original_name: en-us_topic_0218777876.html

.. _en-us_topic_0218777876:

What about Service Level Agreements (SLAs)?
===========================================

There is no end-to-end service level agreement from your cloud endpoints to your local LAN. It is the summary of all SLAs.

You typically have two products as a minimum. One is the network product and the other is Open Telekom Cloud. In this case, you have two different SLAs. If a cloud connectivity broker such as Equinix is involved, you may even have three contracts if the network provider is not able to provide this as a managed service.

There is no such thing as an end-to-end service level agreement. You are using two products with two contracts and separate SLA parameters. The SLA of the network depends on several issues. You can improve network SLAs by using a failure-resistant architecture.

The network SLA is defined by the network provider where you get the contract. Cloud connectivity brokers also have their own SLA.

For Open Telekom Cloud, you generally have an SLA to access Open Telekom Cloud via the PLAS service. The numbers represent the service, not the individual ports, meaning that it only counts when you have redundant access to two data centers and two AZs in a region.
