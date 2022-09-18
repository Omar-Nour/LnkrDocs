Patient URLS
====================

- Patient urls file  **@ patient/api/urls/urls.py**
- URL Path : "api/patient/"
- Patient urls file  has 16 main urls representing all the APIs needed for a Patient
	* register_patient/
		- url for registering a patient uses the API **register_patient** function  in :ref:`views_refactor.py<patient_views_refactor>` file
	* <int:pk>/
		- url for getting patient details using his id that uses the API **get_patient_details** function in :ref:`views_refactor.py<patient_views_refactor>` file

	* <int:pk>/visits/
		- url for getting the patient visits using his id that uses the API **get_patient_visits** function in :ref:`views_refactor.py<patient_views_refactor>` file

	* <int:pk>/visit/create
		- url for creating a patient visit using his id that uses the API **create_patient_visits** function in :ref:`views_refactor.py<patient_views_refactor>` file

	* <int:pk>/labs/
		- url for handling lab results for a patient using his id that uses the API **PatientLabView** in :ref:`views_refactor.py<patient_views_refactor>` file

	* <int:pk>/scans/
		- url for handling scan resultsfor a patient using his id that uses the API **PatientScanView** in :ref:`views_refactor.py<patient_views_refactor>` file

	* <int:pk>/health_records/
		- url handling health records for a patient using his id that uses the API **PatientHealthRecordView** in :ref:`views_refactor.py<patient_views_refactor>` file

	* <int:pk>/reports/
		- url handling visit reports for a patient using his id that uses the API **PatientReportView** in :ref:`views.py<patient_views>` file

	* <int:patient_id>/update/
		- url for updating a patient's data that uses the API **update_patient** function in :ref:`views_refactor.py<patient_views_refactor>` file

	* verify_patient/
		- url for verifying the patient in request data that uses the API **verify_patient** function in :ref:`views.py<patient_views>` file

	* all/
		- url for getting all patients for the current dentist using his email that uses the API **all_patients** in :ref:`views.py<patient_views>` file

	* prescription/
		- url for handling the prescriptions for a patient using his id that uses the API **PrescriptionsViewSet** in :ref:`views.py<patient_views>` file
            - ex : https://lnkrdev.link/api/patient/prescription?patient=1

	* prescription/qr/
		- url for handling the prescriptions for a patient using his uuid that uses the API **PrescriptionsQr** in :ref:`views.py<patient_views>` file
            - ex :  https://lnkrdev.link/api/patient/prescription/qr?uuid=11c33f1c-1472-47d6-af19-7cb2afef6337

	* visits/
		- url for getting the visits of a certain patient using his id that uses the API **VisitViewSet** in :ref:`views.py<patient_views>` file
            - ex : https://lnkrdev.link/api/patient/visits?patient=1

	* treatment_plan/
		- url for resposible for treatment plans for a certain patient using his id that uses the API **TreatmentPlanViewSet**  in :ref:`views.py<patient_views>` file
            - ex : https://lnkrdev.link/api/patient/treatment_plan/?patient=1
        
        * treatment_plan/<int:pk>
		    - url for resposible for a certain treatment plan for a certain patient using the treatment id that uses the API **TreatmentPlanDetails**  in :ref:`views.py<patient_views>` file
            
	



