.. _assets_views:

Assets Views
============================
- Assets views file  **@ assets/api/views.py**
- In the Patient views we mainly used **Django REST framework** , feel free to check the: `Documentaion <https://www.django-rest-framework.org/>`_.


- Patient Views Contains *Seven main Functions:

    - GenderViewSet
    - WeekDayViewSet
    - InsuranceCoViewSet
    - ClinicSpecialityViewSet
    - PatientDiagnosticsViewSet
    - CityViewSet
    - PhysicianSpecialitiesViewSet


**GenderViewSet** 
-----------------

- *GET Functions* : 
    - **get** :  for getting genders


**WeekDayViewSet** 
------------------

- *GET Functions* :
    - **get** : for getting all week days

**InsuranceCoViewSet** 
----------------------

- *GET Functions* :
    - **get** : for getting all insurance companys

**ClinicSpecialityViewSet** 
---------------------------

- *GET Functions* :
    - **get** : for getting all clinic specialities

**PatientDiagnosticsViewSet** 
-----------------------------

- *GET Functions* : 
    - **get** :  for getting all patient diagnosticst

**CityViewSet** 
---------------

- *GET Functions* :
    - **get** : for getting all cities

**PhysicianSpecialitiesViewSet** 
--------------------------------

- *GET Functions* :
    - **get** : for getting all physician specialities


