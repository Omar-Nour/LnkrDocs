.. _patient_views:

Patient Views
============================
- Patient views file  **@ patient/api/views.py**
- In the Patient views we mainly used **Django REST framework** , feel free to check the: `Documentaion <https://www.django-rest-framework.org/>`_.


- Patient Views Contains *Seven main Functions:
    - PrescriptionsViewSet
    - PrescriptionsQr
    - all_patients
    - VisitViewSet
    - TreatmentPlanViewSet
    - TreatmentPlanDetails
    - verify_patient

     
**verify_patient** Function
---------------------------

- **verify_patient** Function is a simple *POST function that takes patient data through the request and returns a message with the problem in data along with HTTP_400_BAD_REQUEST OR an HTTP_200_OK if all data is valid
- JSON Format:
    {
    "uuid": "9e0f9ce5-5276-4d21-abf9-f8dfe430a849",
    "pin_code": "0000"
    }


**PrescriptionsViewSet** 
------------------------
Get and Create Prescription APIs.

- *GET Functions* :
    - **get** : Retrieves all prescriptions for a certain patient using his id
        - ex : /api/patient/prescription?patient=1

- *POST Functions* :
    - **post** : for creating a prescription for a certain patient by the current dentist
    - JSON Format : 
      {
        "insurance":1,
        "diseases": [1,2],
        "patient": 1,
        "drugs":\[
        {
            "comment": "123",
            "dose": "123",
            "frequency": "Daily",
            "general_name": " FluMist 2012-2013"
        },
        {
            "comment": "123",
            "dose": "123",
            "frequency": "Daily",
            "general_name": " FluMist 2012-2013"
        \}
        ]
       }

**PrescriptionsQr** 
-------------------
Prescriptions QR APIs.

- *GET Functions* :
    - **get** : returns the prescription of the given uuid
        - ex : /api/patient/prescription/qr?uuid=11c33f1c-1472-47d6-af19-7cb2afef6337
    - **get_queryset** :  returns all prescripions

- *POST Functions* :
    - **post** : creates a new prescripion
        - JSON Format:


**all_patients** 
----------------
Get all Patients API

- *GET Functions* : 
    - **get** :  returns all patients of the current dentist
    - **retrieve** :  returns a certain request using dentist and request id

**VisitViewSet** 
----------------
Get All Visits API.

- *GET Functions* :
    - **get** : all visits for a certain patient using his id
        - ex : /api/patient/visits?patient=1

- *POST Functions* :
    - **post** : creates a new prescripion
        - JSON Format:

**TreatmentPlanViewSet** 
------------------------
Get Treatment Plan API.

- *GET Functions* :
    - **get** : returns the treatment plans for a certain patient usimg his id
        - ex : api/patient/treatment_plan/?patient=1

**TreatmentPlanDetails** 
------------------------
Get, Update and Delete Treatment Plan

- *GET Functions* :
    - **get** : returns the treatment plan for a certain patient usimg the plan's id

- *POST Functions* :
    - **post** : creates a new TreatmentPlan
    - **update** :  updates a treatment plan
        - JSON Format:
