ClinicAssets Models
==========================

- Assets Models file  **@ assets/models/clinic_assets.py**
- it contains **2 main tables designed as below.** 


Room Table
----------

.. list-table:: **Room Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - name
     - CharField
     - No
   * - number
     - SmallIntegerField
     - No
   * - floor
     - SmallIntegerField
     - No
   * - clinic
     - ForeignKey
     - Clinic



GeneralEvent Table
------------------

.. list-table:: **GeneralEvent Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - title
     - CharField
     - No
   * - location 
     - CharField
     - No
   * - source
     - ForeignKey
     - No
   * - all_day
     - BooleanField
     - No
   * - starts
     - DateTimeField
     - No
   * - ends
     - DateTimeField
     - No

*GeneralEvent Table Contains one display function (display_general_event)*