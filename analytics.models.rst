Analytics Models
====================

- Analytics Models file  **@ analytics/models/models_internal.py**
- it contains **one main table designed as below.** 

Administrator Table
--------------------

.. list-table:: **Administrator Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - uuid
     - UUIDField
     - PrimaryKey
   * - full_name
     - CharField
     - No
   * - clearance
     - CharField
     - No
   * - city
     - CharField
     - No
   * - joined_date
     - DateTimeField
     - No
