.. _patient_views_refactor:

Patient Refactored Views 
=================================
- Patient refactored views file  **@ patient/api/views_refactor.py**
- In the Patient refactored views we mainly used **Django REST framework** , feel free to check the: `Documentaion <https://www.django-rest-framework.org/>`_.


- Patient Refactored Views Contains *Six main Functions:
	- PatientViewSet
	- PatientLabView
	- PatientScanView
	- PatientReportView 
	- PatientHealthRecordView


**PatientViewSet** Function
---------------------------

- *GET Functions* :
    - **get_patient_details** : Returns the personal information of a patient using the patient id
        - Permissions:
            - * A patient can view their personal information.
            - * A doctor can view patients' information.
            - * A superuser can view patients information (update or delete not yet implemented)
        - ex : /api/patient/18
    - **get_patient_visits** :  Returns the patient visits.
        - Permissions:
            - * A patient can only view their visits.
            - * A superuser can view patients visits 

- *POST Functions* :
    - **register_patient** : for creating a patient with full data in request
        - JSON Format :
        {
            "profile": {
                "email": "test_email_2@mail.com",
                "mobile": "22345678910",
                "national_id": "2112233444455",
                "password": "password"
        },
            "full_name": "test_patient_2",
            "age": "20",
            "gender": "1"
        }
    - **update_patient** : *PUT function for updating patient data (partial/full) 

    - **create_patient_visit** : for creating a patient visit using patient id
        - JSON Format :
        {
            "scheduled_date": "2022-06-6T19:22:03.876Z",
            "visit_status":"Confirmed",
            "visit_type":"First Visit"
        }

**PatientLabView** 
------------------
Get and Create Patient lab reports.

- *GET Functions* :
    - **get** : Retrieves all lab reports for a patient using his id

- *POST Functions* :
    - **post** : for creating a lab report for a patient using his id
        - JSON Format : 
      

**PatientScanView** 
-------------------
Get and Create Patient Scan results.

- *GET Functions* :
    - **get** : Retrieves all scan results for a patient using his id

- *POST Functions* :
    - **post** : for creating a scan result for a patient using his id
        - JSON Format : 


**PatientReportView** 
---------------------
Get and Create Patient visit reports.

- *GET Functions* :
    - **get** : Retrieves all reports for a patient using his id

- *POST Functions* :
    - **post** : for creating a report for a patient using his id
        - JSON Format : 

**PatientHealthRecordView** 
---------------------------
Get and Create Patient health records.

- *GET Functions* :
    - **get** : Retrieves all health records for a patient using his id

- *POST Functions* :
    - **post** : for creating a health record for a patient using his id
        - JSON Format : 
        {
            "weight": "200",
            "height": "160",
            "blood_pressure": "30",
            "sugar_level": "30",
            "temperature": "30",
            "oxygen_saturation": "30",
            "other": {"other_attr":"5", "last_attr":"7"}
        }
