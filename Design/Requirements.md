# Requirements
## Functional Requirements
- FR1: If the caregiver does not have internet access, the system shall save their clock-in and clock-out times and locations.
    - Business Requirements: BR1
    - Priority: HIGH
- FR2: If the caregiver does not have internet access, the system shall display their list of tasks for their patient and allow them to mark them complete.
    - Business Requirements: BR2
    - Priority: HIGH
- FR3: Once the caregiver connects to the internet, the system shall upload their saved clock-in and clock-out times and locations to the online web app.
    - Business Requirements: BR1
    - Priority: HIGH
- FR4: If the caregiver needs to take notes, the system shall save them and upload them once they connect to the internet.
    - Business Requirements: BR2
    - Priority: LOW

## Non-functional Requirements
- NR1: The offline web app shall be at least 95 percent available 24/7.
    - Business Requirements: BR2
    - Priority: HIGH
- NR2: Data shall be saved in an average of 5 seconds after the caregiver presses a submit button.
    - Business Requirements: BR1, BR2
    - Priority: MEDIUM
- NR3: Data shall be uploaded in less than 1 minute once the caregiver connects to the internet.
    - Business Requirements: BR1, BR2
    - Priority: MEDIUM
- NR4: A trained user shall be able to clock-in and clock-out in an average of 20 seconds, 95 percent of the time, after 10 minutes of orientation time.
    - Business Requirements: BR1
    - Priority: LOW
- NR5: The application must use the AWS platform.
    - Business Requirements: BR3
    - Priority: HIGH
- NR6: The application must be developed using Ruby on Rails or React.
    - Business Requirements: BR3
    - Priority: HIGH
- NR7: The application must look like the pre-existing web app.
    - Business Requirements: BR3
    - Priority: MEDIUM
- NR8: The application must provide the following functions while offline: clock-in & clock-out, select patient, track location when clocking in and out, view tasks and goals, and add a note
    - Business Requirements: BR4
    - Priority: HIGH
