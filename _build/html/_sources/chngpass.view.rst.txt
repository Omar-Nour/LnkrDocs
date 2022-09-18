.. _chngpass_views:

ChangePass View
========================
- ChangePass views file  **@ auth_/views.py**
- In this view we mainly used **Django REST framework** , feel free to check the: `Documentaion <https://www.django-rest-framework.org/>`_.


- ChangePass View Contains *one main Function:
	- ChangePasswordView

**ChangePasswordView** 
----------------------
An endpoint for changing password.

- **update** : changes a password for the current user
    - JSON Format : 
    {
        "old_password": "test1234",
        "new_password": "test123"
    }
