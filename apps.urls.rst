Apps URLS
==========================

- Dentist urls file  **@ apps/urls.py**
- URL Path : "/"
- Apps urls file  is the main path that connects all paths
- Apps URL specific paths:
	* admin/
		- url for admin page
	* api/token/
		- url for generating tokens

	* api/token/refresh/
		- url for generating token refresh

	* api/change-password/
		- url for cahnging CustomeUser password that uses the API **ChangePasswordView** in :ref:`views.py<chngpass_views>` file

	* api/calendar
		- url for creating calendar visits that uses the API **CalendarViewSet** in :ref:`calendar.py<calendar_views>` file

	* api/requests/
		- url for listing requests that uses the API **AdminRequestsViewSet** in :ref:`dentist.py<dentist_views>` file

	* api/requests/<uuid:request_uuid>/
		- url for handling a certain request that uses the API **AdminRequestsViewSet** in ::ref:`dentist.py<dentist_views>` file

	* api/requests/pending/
		- url for geting pending request that uses the API **AdminRequestsViewSet** in :ref:`dentist.py<dentist_views>` file

	