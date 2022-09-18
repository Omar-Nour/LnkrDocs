.. _supplier_views:

Supplier Views
=======================================
- Supplier views file  **@ supplier/api/views/order.py**
- In the Supplier views we mainly used **Django REST framework** , feel free to check the: `Documentaion <https://www.django-rest-framework.org/>`_.


- Supplier Views Contains *One main Function:
	- OrderViewSet


**OrderViewSet** Function
-------------------------
Get and Create Orders APIs.

- *GET Functions* :
    - **get** : returns all orders of the current dentist

- *POST Functions* :
    - **post** : creates a new order for the current dentist
        - JSON Format:
        [
            {
                "name": "post product 30",
                "quantity": "100",
                "price": 100.5
            },
            {
                "name": "post product 40",
                "quantity": 100,
                "price": 100
            }
        ]