Assets URLS
===================

- Assets urls file  **@ assests/api/urls.py**
- URL Path : "api/assests/"
- Assests urls file  has 7 main urls representing all the APIs needed for Assets
	* gender/
		- url for getting genders that uses the API **GenderViewSet** in :ref:`views.py<assets_views>` file
	* week_day/
		- url for getting all week days that uses the API **WeekDayViewSet** in :ref:`views.py<assets_views>` file

	* insurance/
		- url for getting all insurance companys that uses the API **InsuranceCoViewSet** in :ref:`views.py<assets_views>` file

	* clinic_speciaity/
		- url for getting all clinic specialities that uses the API **ClinicSpecialityViewSett** in :ref:`views.py<assets_views>` file

	* physician_specialities/
		- url for getting all physician specialities that uses the API **PhysicianSpecialitiesViewSet** in :ref:`views.py<assets_views>` file

	* patient_diagnostic/
		- url for getting all patient diagnostics hat uses the API **PatientDiagnosticsViewSet** in :ref:`views.py<assets_views>` file

	* city/
		- url for getting all cities that uses the API **CityViewSet** in :ref:`views.py<assets_views>` file
