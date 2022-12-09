:original_name: en-us_topic_0218777863.html

.. _en-us_topic_0218777863:

Modifying a PLAS (VPN) Connector
================================

Modify the name, bandwidth, and description of the desired PLAS connector.

Prerequisites
-------------

-  A PLAS connector has been created.
-  The PLAS connector is in the **Available** state.
-  If user wants to increase the bandwidth:

   -  The network circuits have to be prepared for the higher bandwidth.
   -  The DC connections have to be prepared for the higher bandwidth.

Procedure
---------

#. Log in to the management console.

#. Choose **Service List** > **Network** > **Private Link Access Service** from the main menu.

#. Choose **Connector** from the navigation pane.

#. Click **Modify** in the **Operation** column of the row that contains the desired PLAS connector.

#. Modify the PLAS connector information as required.

   .. note::

      You can increase or decrease the bandwidth. The bandwidth of the PLAS connector cannot exceed that of the DC connection configured for connecting to the primary location.

   |image1|

   .. table:: **Table 1** Modifiable PLAS connector information

      ===================== ==================
      Category              Parameter
      ===================== ==================
      Connector Information Name
      \                     Description
      \                     Bandwidth (Mbit/s)
      ===================== ==================

#. Click **Submit**.

   .. note::

      The modification does not interrupt services.

.. |image1| image:: /_static/images/en-us_image_0249207697.png
