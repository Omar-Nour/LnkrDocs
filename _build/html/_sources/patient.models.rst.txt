Patient Models
======================

- Patient Models file  **@ patient/models/models_patient.py**
- it contains **three main tables designed as below.** 




Patient Table
-------------

.. list-table:: **Patient Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - full_name
     - CharField
     - No
   * - birthdate
     - DateField
     - No
   * - gender
     - CharField
     - No
   * - profession
     - CharField
     - No
   * - has_card
     - BooleanField
     - No
   * - pin_code
     - CharField
     - No
   * - uuid
     - UUIDField
     - No
   * - home_address
     - ForeignKey
     - Address
   * - work_address
     - ForeignKey
     - Address
   * - profile
     - OneToOneField
     - CustomUser



- Patient Model has One **property function** called **age** to calculate age from birth date




Prescription Table
------------------

.. list-table:: **Prescription Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - notes
     - CharField
     - No
   * - created_date
     - DateTimeField
     - No
   * - uuid
     - UUIDField
     - No
   * - insurance
     - ForeignKey
     - InsuranceCo
   * - drug
     - ManyToManyField
     - Drug
   * - diseases
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



- Prescription Model has **create_QR_code function** that uses **@receiver Decorator** to create the e-prescription and save it @ ** media_cdn/** Directory



TreatmentPlan Table
-------------------

.. list-table:: **TreatmentPlan Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - actions
     - CharField
     - No
   * - total_cost
     - PositiveIntegerField
     - No
   * - paid
     - PositiveIntegerField
     - No
   * - total_paid
     - PositiveIntegerField
     - No
   * - comment
     - CharField
     - No
   * - tooth_numbers
     - JSONField
     - No
   * - created_date
     - DateTimeField
     - No
   * - last_modified
     - DateTimeField
     - No
   * - uuid
     - UUIDField
     - No
   * - patient
     - ForeignKey
     - Patient
   * - dentist
     - ForeignKey
     - Dentist
   * - clinic
     - ForeignKey
     - Clinic

PatientHealthRecord Table
-------------------------

.. list-table:: **PatientHealthRecord Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - uuid
     - UUIDField
     - PrimaryKey
   * - patient
     - ForeignKey
     - Patient
   * - created_date
     - DateTimeField
     - No
   * - weight
     - CharField
     - No
   * - height
     - CharField
     - No
   * - blood_pressure
     - CharField
     - No
   * - sugar_level
     - CharField
     - No
   * - temprature
     - CharField
     - No
   * - oxygen_saturation
     - CharField
     - No
   * - other
     - JSONField
     - No

- PatientHealthRecord Model has One **property function** called **BMI** to calculate the BMI of each user.

PatientLab Table
----------------

.. list-table:: **PatientLab Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - uuid
     - UUIDField
     - PrimaryKey
   * - patient
     - ForeignKey
     - Patient
   * - created_date
     - DateTimeField
     - No
   * - lab_result
     - ImageField
     - (upload_to='labs/')
   * - lab_name
     - CharField
     - No

PatientReport Table
-------------------

.. list-table:: **PatientReport Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - uuid
     - UUIDField
     - PrimaryKey
   * - patient
     - ForeignKey
     - Patient
   * - created_date
     - DateTimeField
     - No
   * - title
     - CharField
     - No
   * - body
     - TextField
     - No

PatientScan Table
-----------------

.. list-table:: **PatientScan Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - uuid
     - UUIDField
     - PrimaryKey
   * - patient
     - ForeignKey
     - Patient
   * - created_date
     - DateTimeField
     - No
   * - scan_result
     - ImageField
     - (upload_to='scans/')
   * - scan_name
     - CharField
     - No