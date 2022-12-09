:original_name: en-us_topic_0218777860.html

.. _en-us_topic_0218777860:

Creating a PLAS (VPN) Connector
===============================

Prerequisites
-------------

-  You have subscribed to the IPLS network of Deutsche Telekom.
-  You have subscribed to a Direct Connect service.

Process
-------


.. figure:: /_static/images/en-us_image_0249207692.png
   :alt: **Figure 1** Creating a PLAS connector

   **Figure 1** Creating a PLAS connector

Procedure
---------

#. Log in to the management console.

#. Choose **Service List** > **Network** > **Private Link Access Service** from the main menu.

#. Choose **Connector** from the navigation pane.

#. Click **Create PLAS Connector**.

#. Set the PLAS connector parameters.

   .. _en-us_topic_0218777860__table8533192195514:

   .. table:: **Table 1** PLAS connector parameters

      +-----------------------+-------------------------+------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      | Category              | Parameter               | Description                                                                                                      | Example                           |
      +=======================+=========================+==================================================================================================================+===================================+
      | Connector Information | Region                  | Indicates the PLAS connector region.                                                                             | eu-de                             |
      +-----------------------+-------------------------+------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      |                       | Name                    | Indicates the PLAS connector name, which must meet the following requirements:                                   | Connector1                        |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | -  Be unique.                                                                                                    |                                   |
      |                       |                         | -  Contain 1 to 64 characters.                                                                                   |                                   |
      |                       |                         | -  Consist of letters, digits, underscores (_), and hyphens (-).                                                 |                                   |
      +-----------------------+-------------------------+------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      |                       | Description             | Indicates the PLAS connector description.                                                                        | This is the first PLAS connector. |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | Length: 0-255 characters                                                                                         |                                   |
      +-----------------------+-------------------------+------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      |                       | Bandwidth (Mbit/s)      | Indicates the bandwidth available for the PLAS connector.                                                        | 1000 Mbit/s                       |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | -  Setting method: Drag the slider or click\ |image1| or\ |image2| or to set Bandwidth.                          |                                   |
      |                       |                         | -  The bandwidth of the PLAS Connector cannot be greater than that of the DC connection in the primary location. |                                   |
      |                       |                         | -  Value range: 10-1000 Mbit/s. Options are as follows: 10, 50, 100, 150, 200, 300, 400, 500, 600, 1000.         |                                   |
      +-----------------------+-------------------------+------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      | Cloud Information     | Provider                | Indicates the cloud provider.                                                                                    | Open Telekom Cloud                |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | Only **Open Telekom Cloud** is currently supported.                                                              |                                   |
      +-----------------------+-------------------------+------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      |                       | Primary Location (AZ)   | Indicates the location and availability zone of the primary physical connection.                                 | Biere (eu-de-01)                  |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | Only **Biere (eu-de-01)** is currently supported.                                                                |                                   |
      +-----------------------+-------------------------+------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      |                       | DC Connection Name      | Indicates the connection name (under Direct Connect) available for the primary location.                         | Direct Connect 1                  |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | Select the Direct Connect name of the Biere location from the drop-down list.                                    |                                   |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | Only DC Connections with related DC Virtual Interface can be selected.                                           |                                   |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | If a DC connection has not been created, click **Create a connection first**.                                    |                                   |
      +-----------------------+-------------------------+------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      |                       | Secondary Location (AZ) | Indicates the location and availability zone of the Secondary physical connection.                               | Magdeburg (eu-de-02)              |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | Only **Magdeburg (eu-de-02)** is currently supported.                                                            |                                   |
      +-----------------------+-------------------------+------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      |                       | DC Connection Name      | Indicates the connection name (under Direct Connect) available for the secondary location.                       | Direct Connect 2                  |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | Select the Direct Connect name of the Magdeburg location from the drop-down list.                                |                                   |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | Only DC Connections with related DC Virtual Interface can be selected.                                           |                                   |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | If a DC connection has not been created, click **Create a connection first**.                                    |                                   |
      +-----------------------+-------------------------+------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      | Network Information   | Type                    | Indicates the network type.                                                                                      | IntraSelect                       |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | Only **IntraSelect** is currently supported.                                                                     |                                   |
      +-----------------------+-------------------------+------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      |                       | Access Location (AZ)    | Indicates the **IntraSelect** access location.                                                                   | Biere (eu-de-01)                  |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | Only **Biere (eu-de-01)** is currently supported.                                                                |                                   |
      +-----------------------+-------------------------+------------------------------------------------------------------------------------------------------------------+-----------------------------------+
      |                       | Network PoP             | Indicates the **IntraSelect** network PoP.                                                                       | Berlin                            |
      |                       |                         |                                                                                                                  |                                   |
      |                       |                         | Only **Berlin** and **Frankfurt** are currently supported.                                                       |                                   |
      +-----------------------+-------------------------+------------------------------------------------------------------------------------------------------------------+-----------------------------------+

   .. _en-us_topic_0218777860__fig62937730154034:

   .. figure:: /_static/images/en-us_image_0249207673.png
      :alt: **Figure 2** PLAS connector parameters (Connector Information)

      **Figure 2** PLAS connector parameters (Connector Information)

   .. _en-us_topic_0218777860__fig810817381204:

   .. figure:: /_static/images/en-us_image_0249207699.png
      :alt: **Figure 3** PLAS connector parameters (Cloud Information)

      **Figure 3** PLAS connector parameters (Cloud Information)

   .. note::

      -  After you configure the bandwidth (as shown in :ref:`Figure 2 <en-us_topic_0218777860__fig62937730154034>`), the system filters two DC connection names. That is, only when the bandwidth of a DC connection is greater than or equal to the configured bandwidth, you can select the corresponding DC Connection.
      -  As :ref:`Figure 3 <en-us_topic_0218777860__fig810817381204>`, only DC connections with a DC interface bound to the same virtual gateway are available for selection. Only the primary and secondary DC connections related to the same DC Virtual Gateway can be selected at the same time.

   .. _en-us_topic_0218777860__fig196272059118:

   .. figure:: /_static/images/en-us_image_0249207687.png
      :alt: **Figure 4** PLAS connector parameters (Network Information)

      **Figure 4** PLAS connector parameters (Network Information)

#. Click **Create Now**.

#. Click **Submit**.

   The created PLAS connector is displayed in the PLAS connector list.

   -  In the beginning, this connector is in the **Processing** state, indicating that the system is processing the connector.
   -  After the creation is complete, the state changes to **Available**.

   .. note::

      Charging begins after the PLAS connector is successfully created.

#. Send the PLAS connector ID (as the PLAS service key) to the IP VPN administrator for further configuration.

   .. note::

      Users will be informed by mail from the IP VPN administrator, when PLAS is enabled.

#. After PLAS is enabled, check whether the hosts at both ends of the connection can communicate with each other. You are advised to test whether your local PC and ECSs in Open Telekom Cloud can be pinged.

.. |image1| image:: /_static/images/en-us_image_0249207696.jpg
.. |image2| image:: /_static/images/en-us_image_0249207712.jpg
