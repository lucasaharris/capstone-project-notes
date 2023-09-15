# Domain Model

![Domain Model](Domain%20Model.png "Offline Documentation Domain Model")

## Classes
- Client: The client is the patient that is being cared for. The application provides their name, their goals, and the caregiver's tasks and services for the visit.
- Client Caregiver: This class represents the user of our application, the caregivers. They provide their information, and then they select the client they are caring for.
- Goal: Goals are set by the caregiver for the client to accomplish before their next visit.
- Task: Tasks are what the caregiver needs to get done during their visit. There are 22 possible tasks, so each task has its own name and ID to differentiate it from the other tasks.
- Visit: The visit information includes when and where the caregiver clocked in and out, the appointment time, any comments provided by an admin, notes provided by the caregiver before clocking out, 
- VisitTask: This class tells the system which tasks were accomplished during which visits with the client.
