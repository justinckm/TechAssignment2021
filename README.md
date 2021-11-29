# Background
Company XYZ Pte Ltd is handling feedback submission for various agency. It provides an online portal for the public to submit the feedback.

# Functional Specs
Design and develop an online portal for feedback submission and a backend module to process the submission for Company XYZ Pte Ltd.
The web portal has 2 main functions:
- submission
- check status

The backend module has 2 main functions:
- process incoming submission
- check submission status


## Portal feedback submission
Each feedback submission requires the following information
- Name
- Email
- Contact number
- Agency name
- Feedback (free text)

There should be basic validation fo the field before submission.

## Portal feedback submission status
User will be able to check their feedback status by filling in their
- Email
- Contact number

All records matching the Email and Contact number will be returned to portal

## Backend module submission processing
Submission processing
- processing need not be realtime
- feedback can be "Accepted" or "Rejected"
- for this assignment, the feedback status can be obtained by invoking the endpoint <http://processfeedback.atwebpages.com/submit.php?feedback=Hello%0AWorld>
- the endpoint is intentionally slowed to return the status response
- the volume of submission usually peak during certain months
- module has to take into account of handling such situation
- auto-scaling is not feasible

## Backend module submission status
Submission status
- return all records matching given Email and Contact number

# Technical Specs
- applicant should use React and Springboot in this assignment
- authentication in the portal is optional. All endpoints can be opened
- Please host your source code in a public repository eg. Github or Bitbucket etc
- You may choose host your application in your preferred server
- Provide a README.md with instructions on running the application locally
