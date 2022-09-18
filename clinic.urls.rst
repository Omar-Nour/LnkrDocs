Clinic URLS
================

- Dentist urls file  **@ dentist/api/urls/clinic_urls.py**
- URL Path : "api/clinic/"
- Dentist urls file is a that has 8 main urls representing all the APIs needed for Clinic Management

	* empty path
		- url for creating a clinic that uses the API **create_clinic** function in :ref:`clinic.py<clinic_views>` file

	* <uuid: clinic_uuid>/
		- url for fetching data of a clinic that uses the API **read_clinic** function in :ref:`clinic.py<clinic_views>` file

	* <uuid: clinic_uuid>/update
		- url for updating clinic data that uses the API **update_clinic** function in :ref:`clinic.py<clinic_views>` file

	* my_clinics/
		- url that returns all clinics associated with the logged in dentist that uses the API **get_my_clinics** function in :ref:`clinic.py<clinic_views>` file

	* <uuid: clinic_uuid>/category/(?P<category_id>.*)/expenses
		- url that fetches all/some of the clinic's expenses that uses the API **ExpensesViewSet** in :ref:`clinic.py<clinic_views>` file

	* <uuid: clinic_uuid>/category/
		- url for getting or creating an expense category that uses the API **DentistExpensesCategoriesViewSet** in :ref:`clinic.py<clinic_views>` file

	* <uuid: clinic_uuid>/category/<uuid: category_uuid>
		- url that retrieves/updates/deletes a Dentist Expense Category that uses the API **DentistExpensesCategoriesDetails** in :ref:`clinic.py<clinic_views>` file

	* <uuid: clinic_uuid>/assistant/
		- url for creating/deleting/updating/listing assistants in a clinic that uses the API **AssistantViewSet** in :ref:`clinic.py<clinic_views>` file


