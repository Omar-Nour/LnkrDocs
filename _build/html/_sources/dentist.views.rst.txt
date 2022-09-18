.. _dentist_views:

Dentist Views
============================
- Dentist views file  **@ dentist/api/views/dentist.py**
- Dentist views file is the most **IMPORTANT** Module in Dentist app as it contain all Query logics and functions.

- In the Dentist views we mainly used **Django REST framework** , feel free to check the: `Documentaion <https://www.django-rest-framework.org/>`_.


- Dentist Views Contains *Five main Functions:
	- create_dentist
	- activate_dentist
	- DentistViewSet
    - RequestsViewSet
    - AdminRequestsViewSet




**create_dentist** Function
-------------------------------

- **create_dentist** Function is a simple *POST function that takes the *request and returns HTTP_201_CREATED *response if the user/dentist created

- creating dentist object process contain *two main operations
	- creating Customuser object
	- then creating dentist object

	**dentist table has OneToOneField Relation with CustomeUser table
- JSON request for this Endpoint is as below: 
{
    "user": {
        "mobile": "01005170441",
        "email": "fekri@main.com",
        "password": "passowrd",
        "national_id": "01005170441"
    },
    "dentist": {
        "full_name": "fekri main",
        "qualifications": "tes qualifications",
        "speciality": [1]

    }
}

**activate_dentist** Function
-------------------------------

- **activate_dentist** Function is a simple *POST function that takes the dentist uuid and tries to activate it and if the user is an admin it would return HTTP_200_OK else it would return HTTP_401_UNAUTHORIZED


**DentistViewSet** 
-------------------------------
Dentist APIs.
Retrieve and update Dentist instance.

- *GET Functions* :
    - **get_patients_for_authenticated_dentist** : Retrieves all the patients that have scheduled a visit with this dentist using dentist id (with pagination) and returns HTTP_200_OK or HTTP_403_FORBIDDEN
    - **get_patients_search** :  Retrieves all the patients that have scheduled a visit with this dentist using dentist id (without pagination) and returns HTTP_200_OK or HTTP_403_FORBIDDEN
    - **get_referred_patients** :  Retrieves all the referrals made by the dentist of dentist_id (This method is only available for superusers) and returns HTTP_200_OK or HTTP_403_FORBIDDEN or HTTP_400_BAD_REQUEST
    - **get_home_analytics** :  get home analytics for dentist (number of patients, prescriptions, orders) using dentist_id and returns HTTP_400_BAD_REQUEST if it fails
    - **get_accounting** :  Get Accounting Data from Dentist filtered by day/month/year and returns HTTP_200_OK or HTTP_403_FORBIDDEN
    - **get_golden_items** :  gets the favourite items for a dentist using dentist id and returns HTTP_200_OK
    - **get_dentist_expenses** :  gets the expense of a certain dentist using dentist_id and returns HTTP_200_OK

- *POST Functions* :
    - **update_dentist** : Partially updates a Dentist with the given uuid and returns HTTP_200_OK or HTTP_400_BAD_REQUEST
    - **create_patient_from_dentist_api** :  Create a patient from the dentist api. Patients created using this method would be associated with the dentist that created them, The association is achieved via a PatientVisit of type referral. returns HTTP_201_CREATED or HTTP_400_BAD_REQUEST
    - **create_prescription** : Create a new prescription for a patient using dentist id and returns HTTP_201_CREATED or HTTP_400_BAD_REQUEST or HTTP_403_FORBIDDEN
    - **create_dentist_expenses** : creates an expense for a dentist using his id and returns HTTP_201_CREATED
    - JSON Format : 
      {
            "salaries": "2000",
            "bills": "300",
            "purchases": "450",
            "other": {"other": "240"}
      } 

**RequestViewSet** 
-------------------------------
- *GET Functions* :
    - **list**
    - **get_queryset** :  returns all requests of a certain dentist using dentist id
    - **retrieve** :  returns a certain request using dentist and request id

- *POST Functions* :
    - **create** : creates a new request with the given dentist id and returns HTTP_200_OK
    - **update** :  updates a request using its uuid (partial/all-data) and returns HTTP_200_OK
    - JSON Format :


**AdminRequestsViewSet** 
------------------------------------
- *GET Functions* :
    - **list**: 
    - **get_queryset** :  returns all requests of all dentists
    - **retrieve** :  returns a certain request using dentist and request id
    - **getPending** : returns pending requests with HTTP_200_OK
    
- *POST Functions* :
    - **update** :  updates a request using its uuid (partial/all-data) and returns HTTP_200_OK
    - JSON Format :