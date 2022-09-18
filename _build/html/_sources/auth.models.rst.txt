Auth Models
=====================

- Auth Models file  **@ auth_/models/user.py**
- it contains **a single table for CustomUsers and a CustomUserManager** 


CustomUser Table
----------------
*Acts as an Abstract table for the required data for any user.*

.. list-table:: **CustomUser Fields**
   :widths: 25 25 50
   :header-rows: 1

   * - Field Name 
     - Type
     - Relation
   * - uuid
     - UUIDField
     - PrimaryKey
   * - email
     - EmailField
     - No
   * - mobile
     - CharField
     - No
   * - national_id
     - CharField
     - No
   * - activated
     - BooleanField
     - No
   * - date_joined
     - DateTimeField
     - No
   * - last_login
     - DateTimeField
     - No
   * - is_admin
     - BooleanField
     - No
   * - is_active
     - BooleanField
     - No
   * - is_staff
     - BooleanField
     - No
   * - is_superuser
     - BooleanField
     - No

This table has an attribute of objects of type CustomUsersManager.

CustomUserManager
-----------------
*A BaseUserManager that has 2 functions to create users.*
  * create_user
      - creates a user from given email and password with regular permissions.

  * create_superuser
      - creates a user from given email and password with admin permissions.
