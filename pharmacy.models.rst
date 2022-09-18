Pharmacy Models
======================

- Pharmacy Models file  **@ pharmacy/models/models_pharmacy.py**
- it contains **two main tables designed as below.** 


Pharmacy Table
--------------

    *Pharmacy Entity Model.As an entity, pharmacy shall include one personnel in charge for now.*

.. list-table:: **Pharmacy Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - name
     - CharField
     - No
   * - address
     - CharField
     - No
   * - working_days_hours
     - JSONField
     - No
   * - phone_number
     - CharField
     - No
   * - registration_id
     - CharField
     - No
   * - joined_date
     - DateTimeField
     - No
   * - uuid
     - UUIDField
     - No
   * - home_address
     - ForeignKey
     - Address



Pharmacist Table
----------------

.. list-table:: **Pharmacist Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - full_name
     - CharField
     - No
   * - synd_id
     - CharField
     - No
   * - qualifications
     - TextField
     - No
   * - joined_date
     - DateTimeField
     - No
   * - uuid
     - UUIDField
     - No
   * - profile
     - OneToOneField
     - CustomUser
   * - pharmacy
     - ForeignKey
     - Pharmacy