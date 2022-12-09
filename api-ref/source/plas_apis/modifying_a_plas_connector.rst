:original_name: en-us_topic_0218811269.html

.. _en-us_topic_0218811269:

Modifying a PLAS Connector
==========================

Function
--------

This API is used to modify a PLAS connector based on the connector ID. Based on the URL returned, you can query the modification progress.

URI
---

-  URI format

   PUT /v1.0/plasconnector/connectors/{connector_id}

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

   +---------------+-----------+-------------------------------+-------------------------------------------------+
   | Parameter     | Mandatory | Type                          | Description                                     |
   +===============+===========+===============================+=================================================+
   | PlasConnector | Yes       | PlasConnectorUpdateReq object | Indicates information about the PLAS connector. |
   +---------------+-----------+-------------------------------+-------------------------------------------------+

The PlasConnectorUpdateReq object has the following attributes.

+-----------+-----------+---------------------------------+-------------------------------------------------------+
| Parameter | Mandatory | Type                            | Description                                           |
+===========+===========+=================================+=======================================================+
| connector | Yes       | PlasConnectorUpdateModel object | Indicates the request for modifying a PLAS connector. |
+-----------+-----------+---------------------------------+-------------------------------------------------------+

The PlasConnectorUpdateModel object has the following attributes.

+-----------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------+
| Parameter       | Mandatory       | Type            | Description                                                                                                               |
+=================+=================+=================+===========================================================================================================================+
| name            | No              | String          | Indicates the name of the PLAS connector name. The name can consist of letters, digits, underscores (_), and hyphens (-). |
|                 |                 |                 |                                                                                                                           |
|                 |                 |                 | The value is a string of 1 to 128 characters.                                                                             |
+-----------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------+
| description     | No              | String          | Indicates the connector description.                                                                                      |
|                 |                 |                 |                                                                                                                           |
|                 |                 |                 | The value is a string of 0 to 255 characters.                                                                             |
+-----------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------+
| bandwidth       | No              | int32           | Indicates the bandwidth in Mbit/s.                                                                                        |
|                 |                 |                 |                                                                                                                           |
|                 |                 |                 | Value range:                                                                                                              |
|                 |                 |                 |                                                                                                                           |
|                 |                 |                 | -  10                                                                                                                     |
|                 |                 |                 | -  50                                                                                                                     |
|                 |                 |                 | -  100                                                                                                                    |
|                 |                 |                 | -  150                                                                                                                    |
|                 |                 |                 | -  200                                                                                                                    |
|                 |                 |                 | -  300                                                                                                                    |
|                 |                 |                 | -  400                                                                                                                    |
|                 |                 |                 | -  500                                                                                                                    |
|                 |                 |                 | -  600                                                                                                                    |
|                 |                 |                 | -  1000                                                                                                                   |
+-----------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------+
| lineId          | No              | String          | Indicates the line ID, which is assigned by the CCR.                                                                      |
|                 |                 |                 |                                                                                                                           |
|                 |                 |                 | The value is a string of 1 to 36 characters.                                                                              |
+-----------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------+

-  Sample request

   .. code-block:: text

      PUT /v1.0/plasconnector/connectors/e7b778a7-5d94-4263-813f-4aec18473a5a HTTP/1.1

   .. code-block:: text

      Content-Type:application/json

   .. code-block:: text

      Accept:application/json;

   .. code-block:: text

      X-Auth-Token:MIIDwAYJKoZIhvcNAQcCoIIDsTCCA60CAQExDTALBglghkgB

   .. code-block:: text

      {

   .. code-block:: text

            "connector" : {

   .. code-block:: text

                "name" :"modifyLiu",

   .. code-block:: text

                "description" : "modifyLiu",

   .. code-block:: text

                "bandwidth" : 11,

   .. code-block:: text

                "networkInfo": {

   .. code-block:: text

                      "lineId":"UUID"

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

      HTTP/1.1 200 OK

   .. code-block:: text

      Content-Type:application/json

   .. code-block:: text

      Cache-Control:no-cache

   .. code-block:: text

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
   | 200 OK         | The PLAS connector is successfully modified.                                             |
   +----------------+------------------------------------------------------------------------------------------+
   | 202 OK         | The request has been accepted for processing, but the processing has not been completed. |
   +----------------+------------------------------------------------------------------------------------------+

-  Abnormal

   +---------------------------+------------------------------------------------------------------------------------------------+
   | Returned Value            | Description                                                                                    |
   +===========================+================================================================================================+
   | 400 Bad Request           | The server failed to process the request.                                                      |
   +---------------------------+------------------------------------------------------------------------------------------------+
   | 500 Internal Server Error | The server encountered an unexpected condition which prevented it from fulfilling the request. |
   +---------------------------+------------------------------------------------------------------------------------------------+
