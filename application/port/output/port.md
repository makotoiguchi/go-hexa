# Port (output.port)

Defines the Output Ports that the application may use.
Port is the Interface that can be invoked by the application.
Output Adapter implementing an Output Port is transparent to the application.

> Port should receive data in Application Domain model format!

> Port must return data in Application Domain model format!

For example:

  - Application service needs to persist data in a Database
    - service was previously initialized, in main, with an Output Adapter that implements an Output Port
    - service invokes an Output Port method
    - Output Adapter is invoked