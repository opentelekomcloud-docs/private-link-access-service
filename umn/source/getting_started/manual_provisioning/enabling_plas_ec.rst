:original_name: en-us_topic_0092087588.html

.. _en-us_topic_0092087588:

Enabling PLAS (EC)
==================

Scenarios
---------

This section describes how to enable a PLAS connection.

Procedure
---------

#. Contact us by `sending us an email or calling us <https://docs.otc.t-systems.com/en-us/public/learnmore.html>`__. Deutsche Telekom will help you set up an Ethernet Connect between Open Telekom Cloud and your data center, office, or collocation environment by using the required bandwidth, such as 100 Mbit/s or 1 Gbit/s. After the connection is created, Deutsche Telekom notifies you of related parameters, for example, **Line ID** (the identification number of the Ethernet Connect) and **S-tag** (tags used to isolate different users on the carrier network).

#. Collect information and submit the application.

   a. .. _en-us_topic_0092087588__li8665141224616:

      Collect information of parameters for enabling Direct Connect.

      .. table:: **Table 1** Parameters required for enabling Direct Connect

         +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------+
         | Parameter             | Description                                                                                                                                                                 | Example Value                        |
         +=======================+=============================================================================================================================================================================+======================================+
         | Domain Name           | For details about how to obtain the domain name, see section :ref:`Obtaining the Domain Name <en-us_topic_0218777853>`.                                                     | abc123                               |
         +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------+
         | Region                | For details about how to obtain the region, see section :ref:`Obtaining Region <en-us_topic_0218777854>`.                                                                   | eu-de                                |
         +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------+
         | Redundancy connection | A redundant connection is required to access Open Telekom Cloud through PLAS. AZ Biere and AZ Magdeburg provide two access points, respectively. The value must be **Yes**. | Yes                                  |
         +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------+
         | VPC ID                | For details about how to obtain its value, see section :ref:`Obtaining the VPC ID <en-us_topic_0218777855>`.                                                                | 13e2e8cb-5894-496c-8688-7b08c485e70b |
         +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------+
         | Port Type             | Specifies the port type. The value can be **1GE** or **10GE**.                                                                                                              | 1GE                                  |
         +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------+
         | Local Subnet          | Specifies the subnet segment of the local VPC connected to Direct Connect.                                                                                                  | 192.168.1.0/24,192.168.51.0/24       |
         |                       |                                                                                                                                                                             |                                      |
         |                       | A maximum of 25 local subnets can be configured.                                                                                                                            |                                      |
         |                       |                                                                                                                                                                             |                                      |
         |                       | The local subnet and remote subnet cannot be in the same network segment.                                                                                                   |                                      |
         +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------+
         | Remote Subnet         | Specifies the tenant subnet. The values must be private IP addresses with subnet masks. Multiple subnets are separated with commas (,).                                     | 192.168.10.0/24,192.168.52.0/24      |
         |                       |                                                                                                                                                                             |                                      |
         |                       | A maximum of 50 remote subnets can be configured.                                                                                                                           |                                      |
         |                       |                                                                                                                                                                             |                                      |
         |                       | The local subnet and remote subnet cannot be in the same network segment.                                                                                                   |                                      |
         +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------+
         | Bandwidth             | Specifies the bandwidth. The maximum value is **1 Gbit/s**.                                                                                                                 | 1 Gbit/s                             |
         +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------+
         | Name                  | Specifies the connection name. The value is a character string of no more than 64 characters that can contain letters, numbers, underscores (_), and hyphens (-).           | directconnect-001                    |
         +-----------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+--------------------------------------+

   b. .. _en-us_topic_0092087588__li91509140478:

      Collect information of parameters for enabling PLAS based on `PLAS Order Form Template <https://docs.otc.t-systems.com/en-us/plas/doc/download/excel/plas-ot.xlsm>`__.

   c. After collecting information listed in substep :ref:`2.a <en-us_topic_0092087588__li8665141224616>` and substep :ref:`2.b <en-us_topic_0092087588__li91509140478>`, you can submit the application for enabling PLAS using either of the following methods:

   -  Emails: `Send us an email <https://docs.otc.t-systems.com/en-us/public/learnmore.html>`__. Fill in enabling PLAS parameters in the email. The subject of the email is "Apply for enabling PLAS."
   -  Hotline: `Call us <https://docs.otc.t-systems.com/en-us/public/learnmore.html>`__ and provide the collected information to the customer service.
   -  Contact the sales personnel. Send the collected information to sales personnel.

#. Wait for the email, customer service, or sales personnel to notify the provisioning result and provide the configuration information about the BGP connection to Open Telekom Cloud.

#. After PLAS is enabled, check whether the hosts at both ends of the connection can communicate with each other. You are advised to test whether your local PC and ECSs in Open Telekom Cloud can be pinged.

   Accounting starts after PLAS is enabled.
