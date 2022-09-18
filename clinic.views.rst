.. _clinic_views:

Clinic Views
====================
- Clinic views file  **@ dentist/api/views/clinic.py**
- In the Clinic views we mainly used **Django REST framework** , feel free to check the: `Documentaion <https://www.django-rest-framework.org/>`_.


- Clinic Views Contains *Five main Functions:
	- ClinicViewSet
	- AssistantViewSet
	- ExpensesViewSet
	- DentistExpensesCategoriesViewSet
	- DentistExpensesCategoriesDetails


**ClinicViewSet** 
-------------------------------
Clinic ViewSet has two main functionalities:
    - get : Read specific clinic using ID
    - post : Create new clinic associated with logged in Dentist

- *Note* : 
1. dentist ID is obtained from the currently authenticated user to add more security on create operation. let a scenario where
an authenticated dentist manipulates the API request by modifying 'dentist_id' to any other dentist ID.

2. creating a clinic with a superuser will break down the logic. a clinic should only be associated with a dentist, so it makes 
no sense to call the following function with superuser account

- *GET Functions* :
    - **read_clinic** : returns the data of a specific clinic using the given uuid and returns an HTTP_200_OK if found.
    - **get_my_clinics** :  returns all clinics associated with the logged in dentist and returns either HTTP_200_OK or HTTP_400_BAD_REQUEST

- *POST Functions* :
    - **create_clinic** : creates a clinic and returns HTTP_201_CREATED or HTTP_400_BAD_REQUEST
    - **update_clinic** :  updates a clinic using uuid (partial/all-data) and returns HTTP_200_OK oR HTTP_400_BAD_REQUEST
    - JSON Format :
    {
    "clinic": {
        "address": {
            "zip_code": "1111",
            "building": "building no. 1",
            "street": "test street",
            "city": "Cairo"
        },
        "name": "Fekri8 Clinic",
        "phone_num": "01271022008",
        "registration_id": 123456789,
        "working_days_hours": {
            "saturday": "[8-12]"
        },
        "specialities": [
            1
        ]
    }
}

**AssistantViewSet** 
-------------------------------

- *GET Functions* :
    - **list**
    - **get_queryset** :  returns all assistants in a clinic using clinic uuid

- *POST Functions* :
    - **create_assistant** : creates a new assistant at the clinic with the given uuid and returns HTTP_201_CREATED or HTTP_400_BAD_REQUEST
    - **update** :  updates an assistant using clinic uuid (partial/all-data) and returns HTTP_200_OK or HTTP_400_BAD_REQUEST
    - JSON Format :
    
    {
    "user_data": {
        "mobile": "01005171551",
        "email": "assistantesra2@lnkr.com",
        "password": "test",
        "national_id": "29006141400777"
    },
    "assistant_data": {
        "full_name": "assistant esraa",
        "clinic_uuid":"f27b1e49-0082-4033-b2c6-0baad3ec8e06"
    }
}

- **destroy** : deletes an assistant using clinic uuid

**ExpensesViewSet** 
-------------------------------
- *GET Functions* :
    - **list**
    - **get_queryset** :  returns all expenses of a certain categoy using category uuid

- *POST Functions* :
    - **create** : creates a new expense with the given category id and returns HTTP_200_OK
    - **update** :  updates an expense using its uuid (partial/all-data) and returns HTTP_200_OK
    - JSON Format :


**DentistExpensesCategoriesViewSet** 
------------------------------------
Retrieve, Update and Delete Dentist Expenses Categories APIs.
Inherits form generics.ListCreateAPIView.

- *GET Functions* :
    - **get** :  gets all Dentist Expenses Categories using clinic uuid and returns HTTP_200_OK or HTTP_400_BAD_REQUEST

- *POST Functions* :
    - **post** : creates a new dentist expense category with the given clinic uuid and returns HTTP_201_CREATED or HTTP_400_BAD_REQUEST
    - JSON Format :


**DentistExpensesCategoriesDetails** 
------------------------------------

Inherits form generics.RetrieveUpdateDestroyAPIView

- *GET Functions* :
    - **get** :  retrieves a Dentist Expense Category using clinic, category uuid and returns HTTP_200_OK or HTTP_400_BAD_REQUEST

- *POST Functions* :
    - **put** : updates a Dentist Expense Category with the given clinic, category uuid and returns HTTP_200_OK or HTTP_400_BAD_REQUEST
    - JSON Format :

- **delete** : deletes an expnse category using clinic and category uuid  nad returns HTTP_200_OK

