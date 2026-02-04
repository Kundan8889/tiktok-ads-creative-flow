
https://github.com/user-attachments/assets/c051f496-df4f-469c-b6fe-0b060e81d748

TikTok Ads Creative Flow (Frontend Assignment)

This project is a small frontend application that simulates a TikTok Ads creative setup flow.

The goal of this assignment is not to build a full Ads Manager, but to demonstrate how I handle:

OAuth-based authentication flows

Conditional validation logic

Real-world API failure scenarios

Clear and user-friendly error handling

The focus is on correctness, clarity, and reasoning rather than visual polish.

What This App Does

The application allows a user to:

Connect a TikTok Ads account using a simulated OAuth flow

Create a minimal ad with required creative details

Enforce business rules directly in the UI

Handle common API and authentication errors gracefully

All APIs and OAuth interactions are mocked to keep the focus on frontend logic.

OAuth Flow (Simulated)

The app includes a Connect TikTok Ads Account button.

Clicking the button simulates an OAuth Authorization Code flow.

A mock access token is generated and stored locally.

Ad submission is blocked until authentication is completed.

Expired or missing tokens are handled with clear user messaging.

No real TikTok account or backend service is required.

Ad Creation & Validation Logic

The ad creation form includes the following fields:

Campaign Name
Required, minimum 3 characters

Objective
Traffic or Conversions

Ad Text
Required, maximum 100 characters

CTA
Required

Music Selection
Validated using a mocked API

Music Rules

Existing music IDs are validated before submission

Custom or uploaded music is simulated with a generated ID

Ads without music are allowed only for the Traffic objective

Music is mandatory for the Conversions objective

Invalid or geo-restricted music IDs return clear, human-readable errors.

Error Handling

The application handles real-world failure scenarios such as:

Missing or expired OAuth tokens

Missing permissions

Invalid or geo-restricted music IDs

Error presentation is designed to be clear:

Field-level issues are shown inline

System-level issues appear as a global error banner

Raw API error responses are never shown to the user.

Success Flow

On successful ad creation, a confirmation message with a generated Ad ID is displayed

The form is reset after success

The submit button is disabled to prevent duplicate submissions

Technical Notes

Built using React

No backend services are used

OAuth and APIs are fully mocked

State is managed locally using React hooks

Styling is intentionally minimal to prioritize clarity and behavior

What I Would Improve With More Time

Add loading skeletons for better UX

Improve retry and recovery flows

Add basic analytics to track common user errors

Demo Video

A short demo video explaining the OAuth flow, validation logic, and error handling is available here:

Demo Video Link:

👉Uploading 04.02.2026_16.15.52_REC.mp4…


How to Run the Project
cd client
npm install
npm run dev

The app will be available at:
http://localhost:5173

Final Note

This project was built under time constraints with a focus on real-world frontend decision-making.
The goal was to demonstrate how I approach authentication, validation, and error handling in production-like scenarios.
