Records Metadatas
=================

About
-----

  Returns the metadatas of a record

  .. code-block:: bash

    /api/v1/records/{databox_id}/{record_id}/metadatas/

  ======================== =====
   Informations
  ======================== =====
   HTTP Method              GET
   Requires Authentication  Yes
  ======================== =====

Parameters
----------

  ======================== ============== =============
   Parameters               Type           Information
  ======================== ============== =============
   databox_id               integer        The databox id of the record
   record_id                integer        The record_id
  ======================== ============== =============

Response Fields
---------------

  ================= ================================
   Field             Description
  ================= ================================
   record_metadata   The list of the metadatas of the record
  ================= ================================

Response sample
---------------

  .. code-block:: javascript

    {
        "meta": {
            "api_version": "1.2",
            "request": "GET /api/v1/records/1/644/metadatas/",
            "response_time": "2012-06-29T17:04:07+02:00",
            "http_code": 200,
            "error_type": null,
            "error_message": null,
            "error_details": null,
            "charset": "UTF-8"
        },
        "response": {
            "record_metadatas": [
            {
                "meta_id": 4437,
                "meta_structure_id": 1,
                "name": "Object",
                "value": "smoke"
            },
            {
                "meta_id": 4438,
                "meta_structure_id": 4,
                "name": "Keywords",
                "value": "fumée"
            },
            {
                "meta_id": 4439,
                "meta_structure_id": 4,
                "name": "Keywords",
                "value": "smoke"
            },
            {
                "meta_id": 4417,
                "meta_structure_id": 20,
                "name": "CameraModel",
                "value": "NIKON D700"
            },
            {
                "meta_id": 4425,
                "meta_structure_id": 23,
                "name": "Recordid",
                "value": "644"
            },
            {
                "meta_id": 4422,
                "meta_structure_id": 24,
                "name": "MimeType",
                "value": "image/jpeg"
            },
            {
                "meta_id": 4423,
                "meta_structure_id": 25,
                "name": "Size",
                "value": "3221035"
            },
            {
                "meta_id": 4424,
                "meta_structure_id": 26,
                "name": "Extension",
                "value": "JPG"
            },
            {
                "meta_id": 4418,
                "meta_structure_id": 27,
                "name": "Width",
                "value": "4256"
            },
            {
                "meta_id": 4419,
                "meta_structure_id": 28,
                "name": "Height",
                "value": "2832"
            },
            {
                "meta_id": 4421,
                "meta_structure_id": 29,
                "name": "Bits",
                "value": "8"
            },
            {
                "meta_id": 4420,
                "meta_structure_id": 30,
                "name": "Channels",
                "value": "3"
            }
            ]
        }
    }