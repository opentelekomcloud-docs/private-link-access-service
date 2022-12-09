:original_name: en-us_topic_0218811268.html

.. _en-us_topic_0218811268:

Querying Details About a PLAS Connector
=======================================

Function
--------

This API is used to query details about a PLAS connector based on the connector ID.

URI
---

-  URI format

   GET /v1.0/plasconnector/connectors/{connector_id}

-  Parameter description

   +-----------------+-----------------+-----------------+----------------------------------------------+
   | Parameter       | Mandatory       | Type            | Description                                  |
   +=================+=================+=================+==============================================+
   | connector_id    | Yes             | String          | Indicates the PLAS connector ID.             |
   |                 |                 |                 |                                              |
   |                 |                 |                 | The value is a string of 1 to 36 characters. |
   +-----------------+-----------------+-----------------+----------------------------------------------+

Request
-------

-  Parameter description

   None

-  Sample request

   .. code-block:: text

      GET /v1.0/plasconnector/connectors/e7b778a7-5d94-4263-813f-4aec18473a5a HTTP/1.1

   .. code-block:: text

      Content-Type:application/json

   .. code-block:: text

      Accept:application/json;

   .. code-block:: text

      X-Auth-Token:MIIDwAYJKoZIhvcNAQcCoIIDsTCCA60CAQExDTALBglghkgB

Response
--------

-  Parameter description

   +-----------+-----------+---------------------------------+-------------------------------------------------+
   | Parameter | Mandatory | Type                            | Description                                     |
   +===========+===========+=================================+=================================================+
   | connector | Yes       | PlasConnectorDetailModel object | Indicates information about the PLAS connector. |
   +-----------+-----------+---------------------------------+-------------------------------------------------+

The PlasConnectorDetailModel object has the following attributes.

+-----------------+-----------------+--------------------+----------------------------------------------------------------------------------------------------------------------+
| Parameter       | Mandatory       | Type               | Description                                                                                                          |
+=================+=================+====================+======================================================================================================================+
| id              | Yes             | String             | Indicates the PLAS connector ID.                                                                                     |
|                 |                 |                    |                                                                                                                      |
|                 |                 |                    | The value is a string of 1 to 36 characters.                                                                         |
+-----------------+-----------------+--------------------+----------------------------------------------------------------------------------------------------------------------+
| tenantId        | Yes             | String             | Indicates the tenant ID.                                                                                             |
|                 |                 |                    |                                                                                                                      |
|                 |                 |                    | The value is a string of 1 to 36 characters.                                                                         |
+-----------------+-----------------+--------------------+----------------------------------------------------------------------------------------------------------------------+
| name            | Yes             | String             | Indicates the name of the PLAS Connector. The name can consist of letters, digits, underscores (_), and hyphens (-). |
|                 |                 |                    |                                                                                                                      |
|                 |                 |                    | The value is a string of 1 to 128 characters.                                                                        |
+-----------------+-----------------+--------------------+----------------------------------------------------------------------------------------------------------------------+
| description     | No              | String             | Indicates the PLAS connector description.                                                                            |
|                 |                 |                    |                                                                                                                      |
|                 |                 |                    | The value is a string of 0 to 255 characters.                                                                        |
+-----------------+-----------------+--------------------+----------------------------------------------------------------------------------------------------------------------+
| bandwidth       | Yes             | int32              | Indicates the bandwidth in Mbit/s.                                                                                   |
|                 |                 |                    |                                                                                                                      |
|                 |                 |                    | Value range:                                                                                                         |
|                 |                 |                    |                                                                                                                      |
|                 |                 |                    | -  10                                                                                                                |
|                 |                 |                    | -  50                                                                                                                |
|                 |                 |                    | -  100                                                                                                               |
|                 |                 |                    | -  150                                                                                                               |
|                 |                 |                    | -  200                                                                                                               |
|                 |                 |                    | -  300                                                                                                               |
|                 |                 |                    | -  400                                                                                                               |
|                 |                 |                    | -  500                                                                                                               |
|                 |                 |                    | -  600                                                                                                               |
|                 |                 |                    | -  1000                                                                                                              |
+-----------------+-----------------+--------------------+----------------------------------------------------------------------------------------------------------------------+
| cloudInfo       | Yes             | CloudInfo object   | Indicates the cloud interconnected with the PLAS connector.                                                          |
+-----------------+-----------------+--------------------+----------------------------------------------------------------------------------------------------------------------+
| networkInfo     | Yes             | NetworkInfo object | Indicates the network interconnected with the PLAS connector.                                                        |
+-----------------+-----------------+--------------------+----------------------------------------------------------------------------------------------------------------------+
| status          | No              | String             | Indicates the PLAS connector status.                                                                                 |
|                 |                 |                    |                                                                                                                      |
|                 |                 |                    | Value range:                                                                                                         |
|                 |                 |                    |                                                                                                                      |
|                 |                 |                    | -  Pending                                                                                                           |
|                 |                 |                    | -  Available                                                                                                         |
|                 |                 |                    | -  Failed                                                                                                            |
|                 |                 |                    | -  Deleting                                                                                                          |
+-----------------+-----------------+--------------------+----------------------------------------------------------------------------------------------------------------------+
| createTime      | No              | String             | Indicates the creation time. The time must be a UNIX timestamp accurate to milliseconds.                             |
|                 |                 |                    |                                                                                                                      |
|                 |                 |                    | The value is a string of 1 to 36 characters.                                                                         |
+-----------------+-----------------+--------------------+----------------------------------------------------------------------------------------------------------------------+

The CloudInfo object has the following attributes.

+-----------------------+-----------------+-----------------+------------------------------------------------------------------------------+
| Parameter             | Mandatory       | Type            | Description                                                                  |
+=======================+=================+=================+==============================================================================+
| provider              | Yes             | String          | Indicates the cloud provider.                                                |
|                       |                 |                 |                                                                              |
|                       |                 |                 | Only **OTC** is currently supported.                                         |
|                       |                 |                 |                                                                              |
|                       |                 |                 | The value is a string of 1 to 64 characters.                                 |
+-----------------------+-----------------+-----------------+------------------------------------------------------------------------------+
| masterLocation        | Yes             | String          | Indicates the primary area that the PCCE connects to.                        |
|                       |                 |                 |                                                                              |
|                       |                 |                 | Only **Biere** and **Magdeburg** are currently supported.                    |
|                       |                 |                 |                                                                              |
|                       |                 |                 | The value is a string of 1 to 128 characters.                                |
+-----------------------+-----------------+-----------------+------------------------------------------------------------------------------+
| masterDirectConnectId | Yes             | String          | Indicates the ID of the Direct Connect link connected to the primary area.   |
|                       |                 |                 |                                                                              |
|                       |                 |                 | The value is a string of 1 to 36 characters.                                 |
+-----------------------+-----------------+-----------------+------------------------------------------------------------------------------+
| slaveLocation         | Yes             | String          | Indicates the secondary area that the PCCE connects to.                      |
|                       |                 |                 |                                                                              |
|                       |                 |                 | Only **Biere** and **Magdeburg** are currently supported.                    |
|                       |                 |                 |                                                                              |
|                       |                 |                 | The value is a string of 1 to 128 characters.                                |
+-----------------------+-----------------+-----------------+------------------------------------------------------------------------------+
| slaveDirectConnectId  | Yes             | String          | Indicates the ID of the Direct Connect link connected to the secondary area. |
|                       |                 |                 |                                                                              |
|                       |                 |                 | The value is a string of 1 to 36 characters.                                 |
+-----------------------+-----------------+-----------------+------------------------------------------------------------------------------+

The NetworkInfo object has the following attributes.

+-----------------+-----------------+-----------------+-----------------------------------------------------------+
| Parameter       | Mandatory       | Type            | Description                                               |
+=================+=================+=================+===========================================================+
| provider        | Yes             | String          | Indicates the network provider.                           |
|                 |                 |                 |                                                           |
|                 |                 |                 | Only **Telekom** is currently supported.                  |
|                 |                 |                 |                                                           |
|                 |                 |                 | The value is a string of 1 to 64 characters.              |
+-----------------+-----------------+-----------------+-----------------------------------------------------------+
| networkDomain   | Yes             | String          | Indicates the network domain.                             |
|                 |                 |                 |                                                           |
|                 |                 |                 | Only **IPLS** is currently supported.                     |
|                 |                 |                 |                                                           |
|                 |                 |                 | The value is a string of 1 to 128 characters.             |
+-----------------+-----------------+-----------------+-----------------------------------------------------------+
| masterLocation  | Yes             | String          | Indicates the primary area that the PCCE connects to.     |
|                 |                 |                 |                                                           |
|                 |                 |                 | Only **Biere** and **Magdeburg** are currently supported. |
|                 |                 |                 |                                                           |
|                 |                 |                 | The value is a string of 1 to 128 characters.             |
+-----------------+-----------------+-----------------+-----------------------------------------------------------+
| slaveLocation   | Yes             | String          | Indicates the secondary area that the PCCE connects to.   |
|                 |                 |                 |                                                           |
|                 |                 |                 | Only **Biere** and **Magdeburg** are currently supported. |
|                 |                 |                 |                                                           |
|                 |                 |                 | The value is a string of 1 to 128 characters.             |
+-----------------+-----------------+-----------------+-----------------------------------------------------------+
| lineId          | No              | String          | Indicates the line ID, which is assigned by the CCR.      |
|                 |                 |                 |                                                           |
|                 |                 |                 | The value is a string of 1 to 36 characters.              |
+-----------------+-----------------+-----------------+-----------------------------------------------------------+

-  Sample response

   .. code-block:: text

      HTTP/1.1 200 OK

   .. code-block:: text

      Content-Type:application/json

   .. code-block:: text

      Cache-Control:no-cache

   .. code-block:: text

   .. code-block:: text

      {

   .. code-block:: text

       "connector": {

   .. code-block:: text

              "id": "uuid",

   .. code-block:: text

              "tenantId": "uuid",

   .. code-block:: text

              "name": "plasconnector-1",

   .. code-block:: text

              "description":"connector description",

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

                  "lineId":"UUID"

   .. code-block:: text

              },

   .. code-block:: text

              "status": "Available",

   .. code-block:: text

              "createTime": "1223445454"

   .. code-block:: text

       }

   .. code-block:: text

      }

Returned Value
--------------

-  Normal

   ============== ==============================================
   Returned Value Description
   ============== ==============================================
   200 OK         Details about the PLAS connector are returned.
   ============== ==============================================

-  Abnormal

   +---------------------------+------------------------------------------------------------------------------------------------+
   | Returned Value            | Description                                                                                    |
   +===========================+================================================================================================+
   | 400 Bad Request           | The server failed to process the request.                                                      |
   +---------------------------+------------------------------------------------------------------------------------------------+
   | 500 Internal Server Error | The server encountered an unexpected condition which prevented it from fulfilling the request. |
   +---------------------------+------------------------------------------------------------------------------------------------+
