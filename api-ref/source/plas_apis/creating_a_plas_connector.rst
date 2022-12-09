:original_name: en-us_topic_0218811265.html

.. _en-us_topic_0218811265:

Creating a PLAS Connector
=========================

Function
--------

This API is used to create a PLAS connector. Based on the URL returned, you can query the creation progress.

URI
---

-  URI format

   POST /v1.0/plasconnector/connectors

-  Parameter description

   None

Request
-------

-  Parameter description

   +----------------------+-----------+-------------------------------+-------------------------------------------------+
   | Parameter            | Mandatory | Type                          | Description                                     |
   +======================+===========+===============================+=================================================+
   | PlasConnectorService | Yes       | PlasConnectorCreateReq object | Indicates information about the PLAS connector. |
   +----------------------+-----------+-------------------------------+-------------------------------------------------+

The PlasConnectorCreateReq object has the following attributes.

+-----------+-----------+-------------------------------+------------------------------------------------------+
| Parameter | Mandatory | Type                          | Description                                          |
+===========+===========+===============================+======================================================+
| connector | Yes       | PlasConnectorBaseModel object | Indicates the request for creating a PLAS connector. |
+-----------+-----------+-------------------------------+------------------------------------------------------+

The PlasConnectorBaseModel object has the following attributes.

+-----------------+-----------------+--------------------+---------------------------------------------------------------------------------------------------------------+
| Parameter       | Mandatory       | Type               | Description                                                                                                   |
+=================+=================+====================+===============================================================================================================+
| name            | Yes             | String             | Indicates the PLAS Connector name. The name can consist of letters, digits, underscores (_), and hyphens (-). |
|                 |                 |                    |                                                                                                               |
|                 |                 |                    | The value is a string of 1 to 64 characters.                                                                  |
+-----------------+-----------------+--------------------+---------------------------------------------------------------------------------------------------------------+
| description     | No              | String             | Indicates the PLAS Connector description.                                                                     |
|                 |                 |                    |                                                                                                               |
|                 |                 |                    | The value is a string of 0 to 255 characters.                                                                 |
+-----------------+-----------------+--------------------+---------------------------------------------------------------------------------------------------------------+
| bandwidth       | Yes             | int32              | Indicates the bandwidth in Mbit/s.                                                                            |
|                 |                 |                    |                                                                                                               |
|                 |                 |                    | Value range:                                                                                                  |
|                 |                 |                    |                                                                                                               |
|                 |                 |                    | -  10                                                                                                         |
|                 |                 |                    | -  50                                                                                                         |
|                 |                 |                    | -  100                                                                                                        |
|                 |                 |                    | -  150                                                                                                        |
|                 |                 |                    | -  200                                                                                                        |
|                 |                 |                    | -  300                                                                                                        |
|                 |                 |                    | -  400                                                                                                        |
|                 |                 |                    | -  500                                                                                                        |
|                 |                 |                    | -  600                                                                                                        |
|                 |                 |                    | -  1000                                                                                                       |
+-----------------+-----------------+--------------------+---------------------------------------------------------------------------------------------------------------+
| cloudInfo       | Yes             | CloudInfo object   | Indicates the cloud interconnected with the PLAS connector.                                                   |
+-----------------+-----------------+--------------------+---------------------------------------------------------------------------------------------------------------+
| networkInfo     | Yes             | NetworkInfo object | Indicates the network interconnected with the PLAS connector.                                                 |
+-----------------+-----------------+--------------------+---------------------------------------------------------------------------------------------------------------+

The CloudInfo object has the following attributes.

+-----------------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------+
| Parameter             | Mandatory       | Type            | Description                                                                                                                             |
+=======================+=================+=================+=========================================================================================================================================+
| provider              | Yes             | String          | Indicates the cloud provider.                                                                                                           |
|                       |                 |                 |                                                                                                                                         |
|                       |                 |                 | Only **OTC** is currently supported.                                                                                                    |
|                       |                 |                 |                                                                                                                                         |
|                       |                 |                 | The value is a string of 1 to 64 characters.                                                                                            |
+-----------------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------+
| masterLocation        | Yes             | String          | Indicates the primary area that the PCCE in the PLAS Connector connects to. This area corresponds to the area of the PLGW in the cloud. |
|                       |                 |                 |                                                                                                                                         |
|                       |                 |                 | Only **Biere** and **Magdeburg** are currently supported.                                                                               |
|                       |                 |                 |                                                                                                                                         |
|                       |                 |                 | The value is a string of 1 to 128 characters.                                                                                           |
+-----------------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------+
| masterDirectConnectId | Yes             | String          | Indicates the ID of the Direct Connect link connected to the primary area.                                                              |
|                       |                 |                 |                                                                                                                                         |
|                       |                 |                 | The value is a string of 1 to 36 characters.                                                                                            |
+-----------------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------+
| slaveLocation         | Yes             | String          | Indicates the secondary area that the PCCE connects to.                                                                                 |
|                       |                 |                 |                                                                                                                                         |
|                       |                 |                 | Only **Biere** and **Magdeburg** are currently supported.                                                                               |
|                       |                 |                 |                                                                                                                                         |
|                       |                 |                 | The value is a string of 1 to 128 characters.                                                                                           |
+-----------------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------+
| slaveDirectConnectId  | Yes             | String          | Indicates the ID of the Direct Connect link connected to the secondary area.                                                            |
|                       |                 |                 |                                                                                                                                         |
|                       |                 |                 | The value is a string of 1 to 36 characters.                                                                                            |
+-----------------------+-----------------+-----------------+-----------------------------------------------------------------------------------------------------------------------------------------+

The NetworkInfo object has the following attributes.

+-----------------+-----------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------+
| Parameter       | Mandatory       | Type            | Description                                                                                                                               |
+=================+=================+=================+===========================================================================================================================================+
| provider        | Yes             | String          | Indicates the network provider.                                                                                                           |
|                 |                 |                 |                                                                                                                                           |
|                 |                 |                 | Only **Telekom** is currently supported.                                                                                                  |
|                 |                 |                 |                                                                                                                                           |
|                 |                 |                 | The value is a string of 1 to 64 characters.                                                                                              |
+-----------------+-----------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------+
| networkDomain   | Yes             | String          | Indicates the network domain.                                                                                                             |
|                 |                 |                 |                                                                                                                                           |
|                 |                 |                 | Only **IPLS** is currently supported.                                                                                                     |
|                 |                 |                 |                                                                                                                                           |
|                 |                 |                 | The value is a string of 1 to 128 characters.                                                                                             |
+-----------------+-----------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------+
| masterLocation  | Yes             | String          | Indicates the primary area that the PCCE in the PLAS Connector connects to. This area corresponds to the area of the PLGW in the cloud.   |
|                 |                 |                 |                                                                                                                                           |
|                 |                 |                 | Only **Biere** and **Magdeburg** are currently supported.                                                                                 |
|                 |                 |                 |                                                                                                                                           |
|                 |                 |                 | The value is a string of 1 to 128 characters.                                                                                             |
+-----------------+-----------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------+
| slaveLocation   | Yes             | String          | Indicates the secondary area that the PCCE in the PLAS Connector connects to. This area corresponds to the area of the PLGW in the cloud. |
|                 |                 |                 |                                                                                                                                           |
|                 |                 |                 | Only **Biere** and **Magdeburg** are currently supported.                                                                                 |
|                 |                 |                 |                                                                                                                                           |
|                 |                 |                 | The value is a string of 1 to 128 characters.                                                                                             |
+-----------------+-----------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------+
| lineId          | No              | String          | Indicates the line ID, which is assigned by the CCR.                                                                                      |
|                 |                 |                 |                                                                                                                                           |
|                 |                 |                 | The value is a string of 1 to 36 characters.                                                                                              |
+-----------------+-----------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------+
| popLocation     | Yes             | String          | Indicates the PoP that the PCNE in the PLAS Connector connects to. This PoP corresponds to the area of the PCNE in the network.           |
|                 |                 |                 |                                                                                                                                           |
|                 |                 |                 | At present, the value can only be Berlin or Frankfurt.                                                                                    |
|                 |                 |                 |                                                                                                                                           |
|                 |                 |                 | Value range: 1-128 charactersAt present, the value can only be Berlin or Frankfurt.                                                       |
|                 |                 |                 |                                                                                                                                           |
|                 |                 |                 | Value range: 1-128 characters                                                                                                             |
+-----------------+-----------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------+

-  Sample request

   .. code-block:: text

      POST /v1.0/plasconnector/connectors HTTP/1.1

   .. code-block:: text

      Content-Type:application/json

   .. code-block:: text

      Accept:application/json;

   .. code-block:: text

      X-Auth-Token:MIIDwAYJKoZIhvcNAQcCoIIDsTCCA60CAQExDTALBglghkgB

   .. code-block:: text

   .. code-block:: text

      {

   .. code-block:: text

       "connector": {

   .. code-block:: text

              "name": "plasconnector-1",

   .. code-block:: text

              "bandwidth": 50,

   .. code-block:: text

              "cloudInfo": {

   .. code-block:: text

                  "provider": "OTC",

   .. code-block:: text

                  "masterLocation": "Biere",

   .. code-block:: text

                  "masterDirectConnectId": "uuid1",

   .. code-block:: text

                  "slaveLocation": "Magdeburg",

   .. code-block:: text

                  "slaveDirectConnectId": "uuid2"

   .. code-block:: text

              },

   .. code-block:: text

              "networkInfo": {

   .. code-block:: text

                  "provider": "Telekom",

   .. code-block:: text

                  "networkDomain": "IPLS",

   .. code-block:: text

                  "masterLocation": "Biere",

   .. code-block:: text

                  "slaveLocation":"Magdeburg",

   .. code-block:: text

                  "lineId":"UUID",

   .. code-block:: text

              "popLocation":"popLocationID"

   .. code-block:: text

              }

   .. code-block:: text

       }

   .. code-block:: text

      }

Response
--------

-  Parameter description

   +-----------------+-----------------+-----------------+------------------------------------------------------------------------+
   | Parameter       | Mandatory       | Type            | Description                                                            |
   +=================+=================+=================+========================================================================+
   | location        | Yes             | String          | Indicates the URL, through which you can query the operation progress. |
   |                 |                 |                 |                                                                        |
   |                 |                 |                 | The value is a string of 1 to 255 characters.                          |
   +-----------------+-----------------+-----------------+------------------------------------------------------------------------+

-  Sample response

   .. code-block:: text

      HTTP/1.1 202 OK

   .. code-block:: text

      Content-Type:application/json

   .. code-block:: text

      Cache-Control:no-cache

   .. code-block:: text

   .. code-block:: text

      {

   .. code-block:: text

        "location":"/v1.0/plasconnector/connector/e7b778a7-5d94-4263-813f-4aec18473a5a/operations/95a44e38-5d61-44ca-a5c4-f241812fbd51"

   .. code-block:: text

      }

Returned Value
--------------

-  Normal

   +----------------+------------------------------------------------------------------------------------------+
   | Returned Value | Description                                                                              |
   +================+==========================================================================================+
   | 202 Accepted   | The request has been accepted for processing, but the processing has not been completed. |
   +----------------+------------------------------------------------------------------------------------------+

-  Abnormal

   +---------------------------+------------------------------------------------------------------------------------------------+
   | Returned Value            | Description                                                                                    |
   +===========================+================================================================================================+
   | 400 Bad Request           | The server failed to process the request.                                                      |
   +---------------------------+------------------------------------------------------------------------------------------------+
   | 500 Internal Server Error | The server encountered an unexpected condition which prevented it from fulfilling the request. |
   +---------------------------+------------------------------------------------------------------------------------------------+
