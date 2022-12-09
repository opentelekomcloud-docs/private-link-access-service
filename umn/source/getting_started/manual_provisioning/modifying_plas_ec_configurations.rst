:original_name: en-us_topic_0218777852.html

.. _en-us_topic_0218777852:

Modifying PLAS (EC) Configurations
==================================

Scenarios
---------

You can apply to modify the PLAS configuration by email or hotline after filling in `PLAS Order Form Template <https://docs.otc.t-systems.com/en-us/plas/doc/download/excel/plas-ot.xlsm>`__. The modifications include:

-  Modify the PLAS bandwidth. The bandwidth can be 100 Mbit/s or 1 Gbit/s.
-  Modify the protocol information, including the BFD switch, BGP AS number, and QinQ protocol type.
-  Modify the local subnet used by Direct Connect.

When modifying PLAS configurations, you need to apply for modifying Direct Connect configurations at the same time.

.. note::

   If you want to modify multiple parameters in one time for PLAS, separate every parameter in one `PLAS Order Form Template <https://docs.otc.t-systems.com/en-us/plas/doc/download/excel/plas-ot.xlsm>`__ file, and attach all the files in one email. For example: *PLAS Modify QinQ Data Order_20180307.xlsx*, *PLAS Modify BGP_AS_NumbQer_Order_20180307.xlsx*, and *PLAS ModifyBFD_Order_20180307.xlsx*.

Procedure
---------

#. .. _en-us_topic_0218777852__en-us_topic_0094013395_li10986134634:

   Collect information about PLAS parameters to be modified. For details, see `PLAS Order Form Template <https://docs.otc.t-systems.com/en-us/plas/doc/download/excel/plas-ot.xlsm>`__.

#. .. _en-us_topic_0218777852__en-us_topic_0094013395_li69243140817:

   Collect information about Direct Connect parameters to be modified. For details, see :ref:`Table 1 <en-us_topic_0218777852__en-us_topic_0094013395_table5755499203>`.

   .. _en-us_topic_0218777852__en-us_topic_0094013395_table5755499203:

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

#. Based on the parameters collected in step :ref:`1 <en-us_topic_0218777852__en-us_topic_0094013395_li10986134634>` and step :ref:`2 <en-us_topic_0218777852__en-us_topic_0094013395_li69243140817>`, modify PLAS configurations using either of the following methods:

   -  Emails: `Send us an email <https://docs.otc.t-systems.com/en-us/public/learnmore.html>`__ with the title "Modifying PLAS configurations".
   -  Hotline: `Call us <https://docs.otc.t-systems.com/en-us/public/learnmore.html>`__ and provide the collected information to the customer service.

#. Wait for the email and obtain the service ticket from the customer.

#. Wait for the notification of the result from the email or customer service.
