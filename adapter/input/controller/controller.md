# controller

Receive input data and invoke the rest of the application

  - Function to create Controller (invoke in main)
  - Defines Controller's input Interface
  - Implements Interface logic
    - validate input data
    - invoke Application Service through a "Port"
      - if we need to pass an argument, it needs to be in Domain model format
      - the response we will get is in Domain model format
