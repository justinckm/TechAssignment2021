# Background
Company XYZ Pte Ltd is handling feedback submission for various agency. It provides an online portal for the public to submit the feedback.

# Functional Specs
Design and develop a **Frontend Module**(Web Portal) for feedback submission and a **Backend module**(API) to process the submission for Company XYZ Pte Ltd. 

The **Web Portal** has 2 main functions:
- create submission (refer to Submission Form)
- check status of past submissions (refer to Submission Status)

The **API** has 2 main functions:
- process incoming submissions (refer to Submission Processing)
- retrieves submission status (refer to Submission Retrieval)

## Submission Form
Each submission form requires the following information:
- Name*
- Email*
- Contact number*
- Agency name
- Feedback (free text)*
There should be basic validation for the fields before submission.
There is no limit to the number of submission by the same user.
* denotes mandatory fields

## Submission Status
User will be able to check their feedback status by filling in their
- Email*
- Contact number*
All records matching the Email and Contact number will be returned to portal.
There should be basic validation for the fields before submission.
* denotes mandatory fields

## Submission Processing
- provide an API endpoint to receive submission
- processing of each submission need not be realtime
- feedback status can be "Accepted" or "Rejected" and can be obtained by invoking the following endpoint https://codeify.dev/submit-feedback.php?feedback=<Feedback Input>
- this stub endpoint is intentionally throttled (latency up to 10secs) to return a response
- ensure that the design is able to handle huge volume of submission usually peak during certain months
- ensure that the user experience is not affected under such scenario
- auto-scaling is not feasible

## Submission Retrieval
- provide an API endpoint to fetch all submission status based on matching  inputs eg.  Email and Contact number
- do consider if the same user submitted more than a thousand submissions

# Technical Specs
- Preferred tech stack:  React and Spring Boot
- The application must be Production Ready
- Host your source code in a public repository eg. Github or Bitbucket etc
- Provide a README.md with instructions on running the application locally
- You would be expected to demonstrate the performance of handling huge volume of submissions
- Host your application in your preferred server (Optional)
- User Authentication in the Portal (Optional)
