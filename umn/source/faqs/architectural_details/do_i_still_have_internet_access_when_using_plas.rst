:original_name: en-us_topic_0092087654.html

.. _en-us_topic_0092087654:

Do I Still Have Internet Access When Using PLAS?
================================================

You can always access your VPCs via the internet. But if you wish to set up a VPN with IPSec, please note that you can only create one VPN per subnet. You need to create different subnets and separate them using a firewall to handle internet traffic vs. private traffic. PLAS or Direct Connect do NOT offer the option to start or serve an IPSec VPN when the Direct Connect link is down. You have to handle the two options in case of a failure.
