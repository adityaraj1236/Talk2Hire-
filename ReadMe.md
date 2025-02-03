Convex: Interview Platform
Welcome to the Convex Interview Platform built with Convex, Next.js, and TypeScript. This platform allows candidates and interviewers to manage and participate in video interviews. It integrates real-time data syncing, authentication, and serverless functions to provide a seamless and efficient interview experience.

✨ Features
User Authentication & Roles: Candidates and Interviewers can log in and manage their profiles.
Real-time Data Syncing: Automatically syncs user data, such as names, emails, and roles.
Serverless Backend: Powered by Convex functions, no need for a traditional backend.
Role-based Access Control: Interviewer and candidate roles ensure appropriate access.
TypeScript Support: Full TypeScript support for better developer experience and type safety.
🔧 Tech Stack
Convex: Reactive database with automatic syncing.
Next.js: React framework for building server-side rendered applications.
TypeScript: Strongly typed superset of JavaScript for better type safety.
Tailwind CSS: Utility-first CSS framework for styling.
Clerk: User authentication and management.
Stream: Video calls, screen sharing, and video recording.
Convex Schema: Serverless database with real-time synchronization.
⚙️ Installation & Setup
Clone the repository

bash
Copy
Edit
git clone https://github.com/adityaraj1236/convex-interview-platform.git
cd convex-interview-platform
Install dependencies

bash
Copy
Edit
npm install
Set up Convex

Sign up for a Convex account at Convex.dev.
Link your project by running:
bash
Copy
Edit
npx convex dev
Run the development server

bash
Copy
Edit
npm run dev
Access the app

Open your browser and navigate to http://localhost:3000.
📂 Project Structure
convex/: Convex schema and serverless functions.
pages/: Next.js pages for the app.
components/: Reusable UI components (e.g., Navbar, MessageBox).
styles/: Tailwind CSS styles for the application.
🔑 Authentication
This platform uses Clerk for authentication. Users can sign in as candidates or interviewers.

Sign in using GitHub or email.
Role-based access control ensures users can only access appropriate sections of the app based on their role.
🌐 Live Demo
Check out the live demo of the platform (if available) here.

📝 Schema Definition
The schema defines a simple users table with:

name: User's name (String)
email: User's email (String)
image: Optional user image (String)
role: Either "candidate" or "interviewer" (Union type)
typescript
Copy
Edit
import { defineSchema, defineTable } from "convex/server";
import { v } from "convex/values";

export default defineSchema({
  users: defineTable({
    name: v.string(),
    email: v.string(),
    image: v.optional(v.string()),
    role: v.union(v.literal("candidate"), v.literal("interviewer")),
  }),
});
📜 License
This project is licensed under the MIT License - see the LICENSE file for details.

🙋‍♂️ Support
For questions or issues, feel free to open an issue on the GitHub Repository.
You can also reach out to the Discord Community for help.
