:original_name: en-us_topic_0218777858.html

.. _en-us_topic_0218777858:

Procedure of Enabling PLAS (VPN)
================================

If your IP VPN network needs to access a VPC on the OTC, use a PLAS to connect them. The process is as follows:

#. Prepare network circuits.

   Work with Deutsche Telekom to set up an IP VPN between Open Telekom Cloud and your data center, office, or collocation environments. Configure the bandwidth from 10 Mbit/s to 1 Gbit/s based on your network requirements. Contact us by your sales personnel, `email, or call <https://docs.otc.t-systems.com/en-us/public/learnmore.html>`__.

#. Create Direct Connect self-service, then create PLAS Connector self-service.

   Create `Direct Connect connections <https://console.otc.t-systems.com/vpc/#/vpc/createPhyDline>`__ (one connection to primary location Biere and the other one to secondary location Magdeburg), then create `PLAS Connector <https://console.otc.t-systems.com/PLAS/plaswebsite/#/create>`__. Then you will get a PLAS Connector ID.

#. Provide the PLAS connector ID for the IP VPN administrator (email: FMB_UCG-Support_Team@telekom.de) to integrate PLAS with the dedicated network.

   Deutsche Telekom and OTC will process your order. After the connection is established, OTC will inform you through your sales or email.

#. Test the connection.

   Verify that the hosts at both ends of the connection can communicate with each other. You are advised to test whether your local PC and ECSs in Open Telekom Cloud can be pinged.
