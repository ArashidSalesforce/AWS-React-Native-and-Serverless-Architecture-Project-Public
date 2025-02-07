# AWS-React-Native-and-Serverless-Architecture-Project

# Evrlift: Proof of Concept for a Fitness Coaching App

## 🚀 Overview
Evrlift was built as a **Proof of Concept (POC)** to explore new technologies and improve my understanding of **React Native, AWS Serverless Architecture, and DynamoDB Single-Table Design**. The goal was to create a **minimal-click** fitness coaching app that integrates essential features like workout management, client tracking, and authentication.

This project allowed me to experiment with **real-time data fetching, scalable backend architecture, and UI/UX optimizations**, while learning about AWS services, authentication flows, and performance optimizations.

## 🌟 Features Implemented
### 🔥 Core Functionality
- **React Native (Expo Ejected)** – Built for **iOS, Android, and Web** using a unified codebase.
- **Authentication & Token Management** – Implemented using **Cognito & AsyncStorage**.
- **Workout Templates** – Created and assigned structured workouts with embedded **YouTube** instructional videos.
- **Client Tracking** – Basic client management with filtering options for progress tracking.
- **Progress Tracking** – Side-by-side progress photo comparisons and stat tracking.

### 🏗️ Backend Architecture
- **AWS AppSync (GraphQL API)** – Managed client-server interactions efficiently.
- **AWS DynamoDB (Single-Table Design)** – Experimented with schema design for cost-effective querying.
- **AWS Lambda** – Backend logic execution for tasks like data fetching and mutations.
- **AWS S3** – Stored images securely and retrieved them dynamically.

### 📊 Database Schema (DynamoDB)
```yaml
PK (Partition Key)          | SK (Sort Key)                | ItemType     | Additional Attributes
---------------------------|-----------------------------|-------------|----------------------
USER#<userId>               | METADATA                     | User        | Role (coach/client), Email...
USER#<userId>               | WORKOUT#<workoutId>          | Workout     | TemplateId, Sets, Reps...
USER#<userId>               | PROGRESS#<progressId>        | Progress    | Weight, Body Fat %, Photos (S3 Links)...
```
### 🔥 Why Single-Table Design?
✅ **Batch Fetching** – Querying related data in a single request.
✅ **Optimized Reads/Writes** – Reduced costs by minimizing unnecessary queries.
✅ **Scalability** – Allowed easy expansion of related entities.

## 🎯 Technologies Explored
- **React Navigation** – For smooth multi-screen transitions.
- **Reanimated & Gesture Handler** – Learned animation and gesture-based interactions.
- **React Query** – Efficient state management and API data caching.
- **Stripe SDK** – Integrated for subscription-based payments.

## 💡 Lessons Learned & Challenges
- **Token Expiry & Refresh** – Implemented an auto-refresh system for expired authentication tokens.
- **Optimizing DynamoDB Queries** – Structured data to avoid costly scans and improve efficiency.
- **Lazy Loading & Pagination** – Reduced API costs by only fetching required data.
- **Cross-Platform UI Adjustments** – Ensured a seamless experience across mobile and web.

## 🚀 Deployment & CI/CD
- **Frontend:** Deployed via **Expo & Fastlane** for iOS/Android.
- **Backend:** Managed via **AWS SAM (Serverless Application Model)**.
- **Automated Testing:** Basic unit testing using Jest.

## 🎯 Next Steps (For Future Exploration)
🔜 **Enhancing Real-Time Updates** – Implementing GraphQL subscriptions for live coaching feedback.
🔜 **Wearable Integrations** – Exploring data sync with Apple Health & Fitbit.
🔜 **Improved Gamification** – Experimenting with ranking and achievement badges.

## 🎉 Summary
Evrlift served as a **learning project** where I explored **React Native, AWS Serverless Architecture, and scalable data design**. While not intended for production, it provided hands-on experience in building a functional fitness coaching app with authentication, client tracking, and workout management.

🚀 **A step forward in understanding scalable, real-world app architecture.** 🚀
