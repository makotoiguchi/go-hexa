# service

Defines the applicaiton logic

Implements Port's Interface methods to, for example:
  - process the input data
    - invoke Domain logic
  - persist or send data
    - use the output adapter configured (Repository, ..) that implements Output Port
  - return a response to Input Adapter (Controller, ..)
