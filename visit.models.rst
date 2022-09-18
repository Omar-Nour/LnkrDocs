Visit Models
====================

- Visit Models file  **@ visit/models.py**
- it contains **two main tables designed as below.** 

PatientVisit Table
------------------

    *Patient Visits to a Clinic.*

.. list-table:: **PatientVisit Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - uuid
     - UUIDField
     - No
   * - scheduled_date
     - DateTimeField
     - No
   * - visit_status
     - CharField
     - No
   * - visit_cost
     - DecimalField
     - No
   * - visit_type
     - CharField
     - No
   * - patient_discount
     - DecimalField
     - No
   * - lnkr_commission
     - DecimalField
     - No
   * - disease
     - ManyToManyField
     - PatientDiagnostics
   * - patient
     - ForeignKey
     - Patient
   * - dentist
     - ForeignKey
     - Dentist
   * - clinic
     - ForeignKey
     - Clinic


Transaction Table
------------------

    *Patient Transaction as done when in Pharmacy.*

.. list-table:: **Transaction Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - otc_purchase
     - CharField
     - No
   * - date
     - DateTimeField
     - No
   * - base_cost
     - DecimalField
     - No
   * - discount_rate
     - DecimalField
     - No
   * - uuid
     - UUIDField
     - No
   * - pharmacy
     - ForeignKey
     - Pharmacy
   * - patient
     - ForeignKey
     - Pharmacy
   * - prescription
     - ForeignKey
     - Prescription


- Transaction Model has One **property function** called **cost** to calculate total cost from base_cost and discount_rate

