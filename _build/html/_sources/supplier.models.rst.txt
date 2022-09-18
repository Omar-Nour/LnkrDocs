Supplier Models
====================

- Supplier Models file  **@ supplier/models/models_supplier.py**
- it contains **3 main tables designed as below.** 


WareHouse Table
----------------
*Contains data about the supplier companies that sell dental materials.*

.. list-table:: **WareHouse Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - uuid
     - UUIDField
     - PrimaryKey
   * - name
     - CharField
     - No
   * - address
     - CharField
     - No
   * - phoneNum
     - PositiveIntegerField
     - No
   * - regID
     - PositiveIntegerField
     - No
   * - joined_date
     - DateTimeField
     - No
   * - city
     - ManyToManyField
     - City
   

Provider Table
---------------
*Personnel In Charge inside the supplier company. Usually the owner.*

.. list-table:: **Provider Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - uuid
     - UUIDField
     - PrimaryKey
   * - full_name
     - CharField
     - No 
   * - joined_date
     - DateTimeField
     - No
   * - user
     - OneToOneField
     - User
   * - warehouse
     - ForeignKey
     - WareHouse
   

Orders Table
-------------
*Stores the orders from warehouses.*

.. list-table:: **Orders Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - uuid
     - UUIDField
     - PrimaryKey
   * - item
     - ManyToManyField
     - Product
   * - created_date
     - DateTimeField
     - No
   * - comment
     - CharField
     - User
   * - warehouse
     - ForeignKey
     - WareHouse
   * - status
     - ForeignKey
     - OrderStatus
   * - dentist
     - ForeignKey
     - Dentist