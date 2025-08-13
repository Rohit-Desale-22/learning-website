# AI Learning Website

A simple AI-based learning platform with:

- Embedded video lessons
- Quizzes
- Clickstream data tracking stored in Firebase

## Features

- **Video Lessons** — Supports both YouTube embeds and uploaded MP4s.
- **Multiple-Choice Quizzes** — Interactive questions based on the lesson content.
- **Instant Feedback** — Score is calculated immediately after quiz submission.
- **Clickstream Data Tracking**:
  - Tracks user clicks, page views, quiz submissions, and video interactions.
  - Logs the user’s IP address for unique visitor analysis.
  - Sends this data to Firebase Firestore for storage.
  - Useful for analyzing learner engagement.

## Tech Stack

- **Frontend:** HTML, CSS, JavaScript  
- **Backend / Hosting:** Firebase Hosting  
- **Database:** Firebase Firestore  
- **IP Tracking Service:** [ipify.org](https://ipify.org)

## Clickstream Data in Firebase

Whenever a user interacts with the site, the following data is stored:

| Field       | Description |
|-------------|-------------|
| `eventType` | Event name (e.g., `quiz_submit`, `video_play`, `button_click`, `page_view`) |
| `timestamp` | UTC time of the interaction |
| `sessionId` | Randomly generated ID to group a single user's session |
| `ip`        | Public IP address of the user |
| `details`   | Extra event-specific info (e.g., score, video ID, clicked button) |
