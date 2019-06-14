# Object-Trigger-Agenda

A simple, minimal, and easy to maintain design pattern for developing an Apex trigger handler.

//Object Trigger
- Single line Apex trigger (No business logic)
- Connects to Object Trigger Agenda and passes all necessary trigger information
  
//Object Trigger Agenda
- Central agenda for processes run via Object Trigger
- Easy for other developers to read and add/remove processes
- Simple to control order of execution and re-order processes
- Prevent recursion with separate control over before and after triggers
  
//Object Shared Resources
- Prep all resources needed for object classes
- Central class methods to eliminate duplicating actions (e.g. SOQL queries) that impact governor limits
- Loaded before processes in Object Trigger Agenda
- Available throughout the execution context via static variables and collections
