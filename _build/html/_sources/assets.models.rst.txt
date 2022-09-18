Assets Models
=====================

- Assets Models file  **@ assets/models/models_assets.py**
- it contains **11 main tables designed as below.** 


WeekDay Table
-------------

.. list-table:: **WeekDay Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - weekday
     - CharField
     - No



InsuranceCo Table
-----------------

.. list-table:: **InsuranceCo Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - insurance_co
     - CharField
     - No


ClinicSpeciality Table
----------------------

.. list-table:: **ClinicSpeciality Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - specialities
     - CharField
     - No


PhysicianSpeciality Table
-------------------------

.. list-table:: **PhysicianSpeciality Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - specialities
     - CharField
     - No


DentistryTags Table
-------------------

.. list-table:: **DentistryTags Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - dentistry_tag
     - CharField
     - No


PatientDiagnostics Table
------------------------

.. list-table:: **PatientDiagnostics Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - disease
     - CharField
     - No


City Table
----------

.. list-table:: **City Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - City
     - CharField
     - No


OrderStatus Table
-----------------

.. list-table:: **OrderStatus Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - status
     - CharField
     - No


Gender Table
------------

.. list-table:: **Gender Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - Gender
     - CharField
     - No


Product Table
-------------

.. list-table:: **Product Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - name
     - CharField
     - No
   * - quantity
     - PositiveSmallIntegerField
     - No
   * - price
     - DecimalField
     - No
   * - created_date
     - DateTimeField
     - No
   * - uuid
     - UUIDField
     - No


Address Table
-------------

.. list-table:: **Address Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - long
     - DecimalField
     - No
   * - lat
     - DecimalField
     - No
   * - city
     - CharField
     - No
   * - zip_code
     - CharField
     - No
   * - street
     - CharField
     - No
   * - building
     - CharField
     - No
   * - floor
     - PositiveSmallIntegerField
     - No