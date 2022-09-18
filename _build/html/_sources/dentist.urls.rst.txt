Dentist URLS
================

- Dentist urls file  **@ dentist/api/urls/dentist_urls.py**
- URL Path : "api/dentist/"
- Dentist urls file  has 16 main urls representing all the APIs needed for a Dentist
	* empty path
		- url for getting all dentists that uses the list API  from **DentistViewSet**  in :ref:`dentist.py<dentist_views>` file
	* signup
		- url for user signup that uses the API **create_dentist** function in :ref:`dentist.py<dentist_views>` file

	* activate/<uuid: dentist_uuid>
		- url for user activation that uses the API **activate_dentist** function in :ref:`views.py<dentist_views>` file

	* <int:dentist_id>/<int:page>/patients
		- url for getting the dentist's patients with pagination that uses the API **get_patients_for_authenticated_dentist** function in :ref:`dentist.py<dentist_views>` file

	* <int:dentist_id>/patients_search
		- url for getting the dentist's patients without pagination that uses the API **get_patients_search** function in :ref:`dentist.py<dentist_views>` file

	* <int:dentist_id>/accounting
		- url for that fetches all the required data for the ccounting page that uses the API **get_accounting** function in :ref:`dentist.py<dentist_views>` file

	* <uuid: dentist_uuid>/update/
		- url for updating dentist data that uses the API **update_dentist** function in ::ref:`dentist.py<dentist_views>` file

	* <int:dentist_id>/create_prescription/
		- url for creating a prescription that uses the API **create_prescription** function in :ref:`dentist.py<dentist_views>` file

	* <int:dentist_id>/get_expenses/
		- url for fetching dentist expense that uses the API **get_dentist_expenses** function in :ref:`dentist.py<dentist_views>` file

	* <int:dentist_id>/create_expenses/
		- url for creating dentist expenses that uses the API **create_dentist_expenses** function in :ref:`dentist.py<dentist_views>` file

	* <int:dentist_id>/referred_patients/
		- url for getting the referred patients that uses the API **get_referred_patients** function in :ref:`dentist.py<dentist_views>` file

	* <int:dentist_id>/create_patient/
		- url for adding dentist patients that uses the API **create_patient_from_dentist_api** function in :ref:`dentist.py<dentist_views>` file

	* <int:dentist_id>/home
		- url for getting the home analytics that uses the API **get_home_analytics** function in :ref:`dentist.py<dentist_views>` file

	* <int:dentist_id>/golden_items
		- url for getting the dentists favourite items that uses the API **get_golden_items** function in :ref:`dentist.py<dentist_views>` file

	* <int:dentist_id>/request
		- url for resposible for dentist requests activation that uses the API **RequestsViewSet**  in :ref:`dentist.py<dentist_views>` file
	



