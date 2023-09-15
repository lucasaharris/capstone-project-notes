# Actors
* caregiver
  * client facing healthcare worker 
  * caregiver uses an array of different personal devices (phone, tablet, laptop)
  * care for patients in the patient's home
  * work in areas with, and or without internet service
  
# Use cases

* UC1: Sign in  
  * Business requirement: BR3
  * Actor: caregiver
  * Flow: Caregiver enters their email and password and is permitted to DocuMentor app. 
  * Why it's a use case: Caregiver's need to sign in to their account in order to authenticate them. 


* UC2: Type in/ select active client
  * Business requirement: BR2
  * Actor: caregiver
  * Flow: Caregiver types in their currrent patient's name. 
  * Why it's a use case: If data (client list) has not been synced up while user is online, then the drop down list of clients will not appear. The user       will have to manually enter their patients name as this data cannot be accessed while offline. 


* UC3: Express clock in
  * Business requirement: BR1
  * Actor: caregiver
  * Flow: Caregiver can enter in/select their client's name, service performed, and location, then express clock in. After caregiver presses clock 
    in button they are prompted with a summary screen (service, caregiver, time clocked in, blank notes block)
  * Why it's a use case: One of the primary business requirements is that caregiver's can clock in while offline. It is typically the first thing users do     after signing in. Caregiver's will need to manually enter their location in order for the geo tracking feature to function offline. 
  
    
* UC4: Express clock out
  * Business requirement: BR1
  * Actor: caregiver
  * Flow: Caregiver presses 'enter note' and can type in an overall note for the visit. Then they are presented with 'clock out' button. They press 'clock     out' and are taken back to home screen.
  * Why it's a use case: Like clocking in, clocking out is also an essential business requirement. The flow from the user's perspective will look the same.


* UC5: Modify note
  * Business requirement: BR2
  * Actor: caregiver
  * Flow: Caregiver can retype their note then press 'modify note' for the new note to be saved. This option is only visible  to the client within two         hours of clocking out.
  * Why it's a use case: If the caregiver makes a mistake, or thinks of adding more to the note later on, then they should be able to modify it. 


* UC6: Add tasks
  * Business requirement: BR2 
  * Actor: caregiver
  * Flow: Caregiver can select a task (Hygiene- bed/sponge bath, Dress - Assist w dressing ....) from a drop down menu to be added to 
  a list of tasks.
  * Why it's a use case: This helps caregiver's keep track of what their patient has accomplished/ is working on throughout their visit. 
  
  
* UC7: Add goals
  * Business requirement: BR2 
  * Actor: caregiver
  * Flow: Caregiver can select a goal from a drop down menu. Once they select a goal, they are prompted to enter their strategy used, select
  an outcome (succesful, succesful with assistance, unsucessful), enter a note, then save the outcome.
  * Why it's a use case: Caregivers need to keep track of their client's progress. 
  
 
  
