# main

Initializes everything!

For example:
  - Load env porperties
  - Create DB connection
  - init dependencies
    - init user repository with DB connection
    - init user service with repository
    - init users controller with service
  - Create Router
  - init routes with controller
  - Start Router on a port
