Internal Models
=====================

- Internal Models file  **@ internal/models/models_internal.py**
- it contains **three main tables designed as below.** 

OperationsExecutive Table
-------------------------

*OperationsExecutive model is dedicated to operation executives with restricted permissions*

.. list-table:: **OperationsExecutive Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - full_name
     - CharField
     - No
   * - city
     - CharField
     - No
   * - joined_date
     - DateTimeField
     - No
   * - profile
     - ForeignKey
     - CustomUser


DentistContract Table
---------------------

*DentistContract model is responsible for reporting any information that's related to dentists in service*

.. list-table:: **DentistContract Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - start_of_contract
     - DateTimeField
     - No
   * - end_of_contract
     - DateTimeField
     - No
   * - dentist
     - ForeignKey
     - Dentist
   * - operations_executive
     - ForeignKey
     - OperationsExecutive


Administrator Table
-------------------


.. list-table:: **Administrator Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
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
   * - uuid
     - UUIDField
     - No