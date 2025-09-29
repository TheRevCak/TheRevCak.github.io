Air Force Curriculum Design Tool - User Guide (v2.0 - Collaborative Edition)


Page 1: Introduction to a Collaborative Platform

1.1. Overview
Welcome to the next generation of the Air Force Curriculum Design Tool! This version has been completely rebuilt as a real-time, collaborative platform designed for modern curriculum development teams. It moves beyond a single-user tool to a shared, cloud-based workspace where multiple designers and managers can build and modify course curricula simultaneously.

The core functionality remains: an intuitive, task-board interface to visually organize content and automate time calculations. However, with the integration of a cloud backend, your data is now centralized, secure, and always in sync across your entire team.

1.2. Key Enhancements
Real-Time Collaboration: Multiple users can work on the same course at the same time. Changes made by one user are instantly visible to everyone else.

Cloud Data Storage: Your curriculum data is no longer stored in your browser. It's saved in a secure, central cloud database, meaning you can access your work from any computer.

Full Drag-and-Drop: Reorder objectives within a module or teaching steps within an objective. The new order is saved automatically and synchronized for all users.

Persistent Data: All edits to titles and times are saved instantly to the cloud. There is no "save" button—your work is always preserved.

Page 2: Setup & Configuration

2.1. One-Time Firebase Setup (Required)

To power the new collaborative features, the application uses Google Firebase, a secure and scalable cloud platform. A designated administrator will need to perform this free, one-time setup.

Step 1: Create a Firebase Project

Go to the Firebase Console.

Click "Add project" and give it a name (e.g., "AF Curriculum Tool").

Follow the on-screen steps. You can disable Google Analytics if you wish.

Step 2: Create a Firestore Database

Inside your new project, go to the "Build" section on the left and click "Firestore Database".

Click "Create database".

Start in Test mode. This allows open access for development. You can secure it later with security rules.

Choose a location for your database (a us-central option is recommended).

Step 3: Get Your Project Configuration

In your Firebase project, go to "Project Settings" (click the gear icon at the top of the left sidebar).

In the "General" tab, scroll down to "Your apps".

Click the web icon (</>) to create a new web app.

Give it a nickname (e.g., "Curriculum App") and click "Register app".

Firebase will provide you with a firebaseConfig object. It will look like this:

const firebaseConfig = {
  apiKey: "AIzaSy...",
  authDomain: "your-project.firebaseapp.com",
  projectId: "your-project-id",
  // ... and so on
};

Step 4: Add Configuration to index.html

Open the index.html file in a text editor.

Find the firebaseConfig object near the top of the <script type="module"> section.

Carefully copy and paste the values from your Firebase project into the placeholder firebaseConfig object in the file.

Save the index.html file. Your application is now connected to the cloud!

Page 3: Features in a Collaborative Environment

3.1. Working as a Team

Shared Workspace: To collaborate, every team member must use an index.html file that has been configured with the exact same Firebase Project ID. The easiest way to ensure this is to have the administrator configure one file and then distribute it to the team.

Live Updates: When a colleague drags an objective, adds a teaching step, or changes a time, you will see the update on your screen within seconds, without needing to refresh the page.

Share Your Project ID: Click the "Share" button in the header to easily view and copy your project's ID, which is the key to your shared workspace.

3.2. Future-Ready Features
This new platform is designed for growth. The following advanced features are now possible and can be implemented in future updates:

Version History: The system can be configured to take snapshots of the curriculum, allowing you to review and restore previous versions of a module or the entire course.

PDF Exports & Dashboards: The centralized data can be used to generate professional PDF exports and visual dashboards for leadership, showing time breakdowns and resource allocation.

Audit Trails: By upgrading to a full user login system (e.g., sign-in with email), every change can be logged with the user's name and a timestamp, providing a complete history of curriculum modifications.

Page 4: Technical Details & FAQ

4.1. Data Management in the Cloud

No More localStorage: The application no longer uses your browser's local storage. All data is sent to and received from your Firestore database in real-time.

Benefits:

Accessibility: Access your data from any device.

Data Safety: Your data is safe in the cloud and not at risk of being cleared with your browser cache.

Scalability: The system can now handle much larger and more complex course structures.

4.2. Frequently Asked Questions (FAQ)
Is this still free?
Yes. The Firebase "Spark Plan" (the free tier) is extremely generous and is more than sufficient for the needs of most curriculum design teams, offering a significant amount of reads, writes, and storage at no cost.

How do I share the curriculum with a colleague now?
Once you have configured the index.html file with your Firebase project keys, you can simply send them that same HTML file. When they open it, it will automatically connect to your shared cloud database. Alternatively, you can host the file on a platform like GitHub Pages for even easier access.

What if two people try to edit the exact same thing at the same time?
Firestore is designed to handle this. For text editing, it uses a "last write wins" model, meaning the last change to be saved will be the one that all users see. For drag-and-drop reordering, the operations are transactional, ensuring the list order remains consistent for everyone.
