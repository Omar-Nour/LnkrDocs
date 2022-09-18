Dentist Models
==================

- Dentist Models file  **@ dentist/models/models_dentist.py**
- it contains **eight main tables designed as below.** 


Clinic Table
------------
*Clinic Entity Model.As an entity, Clinic shall include multiple physicians, assistants, and rooms.*



.. list-table:: **Clinic Fields**
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
   * - phoneNum
     - PositiveBigIntegerField
     - No
   * - regID
     - PositiveBigIntegerField
     - No
   * - joined_date
     - DateTimeField
     - No
   * - uuid
     - UUIDField
     - No
   * - working_days
     - ManyToManyField
     - WeekDay
   * - generic_event
     - ManyToManyField
     - GeneralEvent
   * - room
     - ManyToManyField
     - Room
   * - speciality
     - ManyToManyField
     - ClinicSpeciality
   * - city
     - ManyToManyField
     - City



*Clinic Table Contain Three display functions (display_working_days, display_speciality, display_city)*

.. image:: /images/clinic_admin.png
	:alt: clinic admin
	:align: center



ClinicOwner Table
-----------------
*Clinic Owner Model.The one managing the whole clinic.*

.. list-table:: **Clinic Owner Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - full_name
     - CharField
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
   * - clinic
     - OneToOneField
     - Clinic




*ClinicOwner Table Contain Three display functions (display_clinics, display_username)*

.. image:: /images/clinic_owner.png
	:alt: clinic owner
	:align: center



Dentist Table
-------------
*Dentist Table is the main table in dentist module and the most important one, structured as below*

.. list-table:: **Dentist Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - full_name
     - CharField
     - No
   * - syndID
     - PositiveIntegerField
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
   * - speciality
     - ManyToManyField
     - PhysicianSpeciality
   * - profile
     - OneToOneField
     - CustomUser
   * - clinic
     - ManyToManyField
     - Clinic




*Dentist Table Contain Three display functions (display_clinics, display_username, display_speciality)*

.. image:: /images/dentist_admin.png
	:alt: dentist
	:align: center




Assistant Table
---------------

*Assistant is secondary table for dentist assistant*

.. list-table:: **Assistant Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - full_name
     - CharField
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
   * - clinic
     - ForeignKey
     - Clinic




*Assistant Table Contain Three display functions (display_username)*

.. image:: /images/assistant_admin.png
	:alt: dentist
	:align: center


DentistExpenses Table
---------------------
*Includes all of the expenses for a dentist.*

.. list-table:: **DentistExpenses Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - uuid
     - UUIDField
     - No
   * - created_date
     - DateTimeField
     - No
   
   * - Category
     - ForeignKey
     - DentistExpensesCategories
   * - Name
     - CharField
     - No
   * - expense
     - CharField
     - No
   * - comment
     - CharField
     - No

.. image:: /images/dentist_expenses_admin.png
	:alt: dentist
	:align: center

DentistExpensesCategories Table
-------------------------------
*Includes all of the categories for expenses.*

.. list-table:: **DentistExpensesCategories Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - uuid
     - UUIDField
     - No
   * - created_date
     - DateTimeField
     - No
   * - name
     - CharField
     - No
   * - description
     - TextField
     - No
   * - clinic
     - ForeignKey
     - Clinic

.. image:: /images/dentist_expenses_categories_admin.png
	:alt: dentist
	:align: center


DentistRequests Table
---------------------
*Includes all of the requests of dentists.*

.. list-table:: **DentistRequests Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - uuid
     - UUIDField
     - No
   * - created_date
     - DateTimeField
     - No
   * - title
     - CharField
     - No
   * - request
     - TextField
     - No
   * - dentist
     - ForeignKey
     - Dentist
   * - comments
     - TextField
     - No
   * - done
     - BooleanField
     - No

.. image:: /images/dentist_requests_admin.png
	:alt: dentist
	:align: center

GoldenItem Table
---------------------
*Includes all of the favourite drugs for dentists.*

.. list-table:: **GoldenItem Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - dentist
     - ForeignKey
     - Dentist
   * - items
     - JSONField
     - No
   
The items field must be the same as prescription.drug:

[
    {
       - 'drug_id': 1,
       - 'dosage': 2,
       - 'dosage_format': 'tablets',
       - 'frequency': 3,
       - 'frequency_duration': [days, weeks],
       - 'duration_how_long': 10,
       - 'food_placement': 'before',
       - 'directions': [],
       - 'comments': 'text',
    },
]

.. image:: /images/golden_item_admin.png
	:alt: dentist
	:align: center




  
