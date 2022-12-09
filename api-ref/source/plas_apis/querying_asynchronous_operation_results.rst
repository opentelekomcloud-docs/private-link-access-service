:original_name: en-us_topic_0218811271.html

.. _en-us_topic_0218811271:

Querying Asynchronous Operation Results
=======================================

Function
--------

This API is used to query asynchronous operation results.

URI
---

-  URI format

   GET /v1.0/plasconnector/connectors/{connector_id}/operations/{operation_id}

-  Parameter description

   +-----------------+-----------------+-----------------+----------------------------------------------+
   | Parameter       | Mandatory       | Type            | Description                                  |
   +=================+=================+=================+==============================================+
   | connector_id    | Yes             | String          | Indicates the PLAS connector ID.             |
   |                 |                 |                 |                                              |
   |                 |                 |                 | The value is a string of 1 to 36 characters. |
   +-----------------+-----------------+-----------------+----------------------------------------------+
   | operation_id    | Yes             | String          | Indicates the operation ID.                  |
   |                 |                 |                 |                                              |
   |                 |                 |                 | The value is a string of 1 to 36 characters. |
   +-----------------+-----------------+-----------------+----------------------------------------------+

Request
-------

-  Parameter description

   None

-  Sample request

   .. code-block:: text

      GET /v1.0/plasconnector/connectors/e7b778a7-5d94-4263-813f-4aec18473a5a/operations/95a44e38-5d61-44ca-a5c4-f241812fbd51 HTTP/1.1

   .. code-block:: text

      Content-Type:application/json

   .. code-block:: text

      Accept:application/json;

   .. code-block:: text

      X-Auth-Token:MIIDwAYJKoZIhvcNAQcCoIIDsTCCA60CAQExDTALBglghkgB

Response
--------

-  Parameter description

   +-----------------+-----------------+-----------------+----------------------------------------------------+
   | Parameter       | Mandatory       | Type            | Description                                        |
   +=================+=================+=================+====================================================+
   | operationId     | Yes             | String          | Indicates the operation ID.                        |
   |                 |                 |                 |                                                    |
   |                 |                 |                 | The value is a string of 1 to 36 characters.       |
   +-----------------+-----------------+-----------------+----------------------------------------------------+
   | operationType   | Yes             | String          | Indicates the operation type.                      |
   |                 |                 |                 |                                                    |
   |                 |                 |                 | Value range:                                       |
   |                 |                 |                 |                                                    |
   |                 |                 |                 | -  Create                                          |
   |                 |                 |                 | -  Delete                                          |
   |                 |                 |                 | -  Update                                          |
   +-----------------+-----------------+-----------------+----------------------------------------------------+
   | finished        | Yes             | boolean         | Specifies whether the operation is successful.     |
   |                 |                 |                 |                                                    |
   |                 |                 |                 | Value range:                                       |
   |                 |                 |                 |                                                    |
   |                 |                 |                 | -  true                                            |
   |                 |                 |                 | -  false                                           |
   +-----------------+-----------------+-----------------+----------------------------------------------------+
   | operateAt       | No              | String          | Indicates the operation time in UNIX time format.  |
   |                 |                 |                 |                                                    |
   |                 |                 |                 | The value is a string of 1 to 36 characters.       |
   +-----------------+-----------------+-----------------+----------------------------------------------------+
   | finishedAt      | No              | String          | Indicates the completion time in UNIX time format. |
   |                 |                 |                 |                                                    |
   |                 |                 |                 | The value is a string of 1 to 36 characters.       |
   +-----------------+-----------------+-----------------+----------------------------------------------------+
   | result          | No              | Result object   | Indicates the operation result.                    |
   +-----------------+-----------------+-----------------+----------------------------------------------------+

The Result object has the following attributes.

+-----------------+-----------------+-----------------+-----------------------------------------------+
| Parameter       | Mandatory       | Type            | Description                                   |
+=================+=================+=================+===============================================+
| result          | No              | String          | Indicates the operation result.               |
|                 |                 |                 |                                               |
|                 |                 |                 | Value range:                                  |
|                 |                 |                 |                                               |
|                 |                 |                 | -  success                                    |
|                 |                 |                 | -  failed                                     |
+-----------------+-----------------+-----------------+-----------------------------------------------+
| reason          | No              | String          | Indicates the reason.                         |
|                 |                 |                 |                                               |
|                 |                 |                 | The value is a string of 0 to 255 characters. |
+-----------------+-----------------+-----------------+-----------------------------------------------+

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

        "operationId": "95a44e38-5d61-44ca-a5c4-f241812fbd51",

   .. code-block:: text

        "operationType": "create",

   .. code-block:: text

        "operateAt": "1517274000",

   .. code-block:: text

        "finishedAt": "1517274020"

   .. code-block:: text

        "finished": true,

   .. code-block:: text

        "result": {

   .. code-block:: text

            "result": "success",

   .. code-block:: text

        "reason": ""

   .. code-block:: text

        }

   .. code-block:: text

      }

Returned Value
--------------

-  Normal

   ============== =======================================
   Returned Value Description
   ============== =======================================
   200 OK         The operation is successfully returned.
   ============== =======================================

-  Abnormal

   +---------------------------+------------------------------------------------------------------------------------------------+
   | Returned Value            | Description                                                                                    |
   +===========================+================================================================================================+
   | 400 Bad Request           | The server failed to process the request.                                                      |
   +---------------------------+------------------------------------------------------------------------------------------------+
   | 500 Internal Server Error | The server encountered an unexpected condition which prevented it from fulfilling the request. |
   +---------------------------+------------------------------------------------------------------------------------------------+
