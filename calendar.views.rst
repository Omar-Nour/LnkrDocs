.. _calendar_views:

Calendar Views
========================
- Calendar views file  **@ dentist/api/views/calendar.py**
- In the Calendar views we mainly used **Django REST framework** , feel free to check the: `Documentaion <https://www.django-rest-framework.org/>`_.


- Calendar Views Contains *one main Function:
	- CalendarViewSet

**CalendarViewSet** 
-------------------------------

- Has *POST, GET functions that takes the request and responds with :
    - HTTP_200_OK : if sucessful GET
    - HTTP_400_BAD_REQUEST : if POSTing a visit in a wrong timming
    - JSON Format :
        {
            'success': True,
            'data': data,
            'message': message
        }

- JSON request for this Endpoint is as below: 
{
   "title": "fekri event",
   "location": "Dummy",
   "all_day": false,
   "id": 1,
   "type": "event",
   "source": 0,
   "cost": 100,
   "visit_status": "Confirmed",
   "start": "2022-05-09T16:30:18.000Z",
   "end": "2022-05-09T16:30:18.000Z"
}

*Note* : type parameter could be event/visit