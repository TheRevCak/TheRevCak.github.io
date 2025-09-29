Air Force Curriculum Design Tool - User Guide


Page 1: Introduction & Core Concepts

1.1. Overview
Welcome to the Air Force Curriculum Design Tool! This is a dynamic, web-based application designed to streamline the process of creating, managing, and modifying course curricula. It provides an intuitive, task-board-style interface that allows curriculum developers and managers to visually organize course content, track instructional time, and automatically generate reports on any changes made.

The tool was built to replace static documents and spreadsheets, offering a more fluid and responsive workflow. By visualizing the course structure and automating time calculations, it helps ensure that curricula are well-paced, comprehensive, and easy to analyze for leadership review.

1.2. Intended Audience
This application is primarily designed for:

Curriculum Development Managers: To oversee course structure, total instructional time, and the logical flow of content.

Instructional Designers & Course Developers: To build, rearrange, and refine modules, objectives, and teaching steps in a flexible environment.

Leadership & Review Personnel: To quickly understand the impact of curriculum changes through detailed, auto-generated summary reports.

While it was developed with the specific needs of Air Force curriculum management in mind, its design is versatile enough for any educational or training organization that requires a structured approach to course planning.

1.3. Core Concepts
The application organizes your curriculum into a clear hierarchy. Understanding these levels is key to using the tool effectively.

Modules: The highest-level container, representing a major section of a course (e.g., "Module 1: Basic Aerodynamics"). A course is typically made up of multiple modules.

Objectives: Specific, measurable learning goals that must be achieved within each module (e.g., "Objective 1.1: Understand the Principles of Lift"). The order of objectives defines the learning path.

Teaching Steps: These are the individual activities, lectures, practical exercises, or simulations required to meet an objective (e.g., "Introduction to Airfoils," "Bernoulli's Principle Activity"). Each step has an associated time value.

Page 2: Features in Detail
2.1. Visual Curriculum Management
The primary interface is a visual board that allows you to see your entire course structure at a glance.

Hierarchical Layout: Modules, objectives, and steps are nested visually, making the relationships between them immediately clear.

Drag-and-Drop Interface: This is the core of the tool's flexibility.

Reorder Objectives: Effortlessly drag and drop objectives within a module to change the instructional flow. The workflow visualization lines will automatically redraw to reflect the new sequence.

Move Teaching Steps: Drag a teaching step from one objective to another. This is useful when you realize an activity is better suited to a different learning goal.

In-line Editing: All text fields for titles and times are editable directly on the board. There are no pop-ups or separate screens, allowing for rapid changes.

2.2. Automatic Time Aggregation
Manual time calculation is prone to error. This tool automates the entire process.

Step-Level Timing: You only need to enter the duration in minutes for each individual Teaching Step.

Objective Totals: The tool automatically sums the times of all steps within an objective and displays the total in a green lozenge.

Module Totals: The total time for all objectives within a module is calculated and displayed prominently in a blue lozenge in the module header.

Live Updates: All time totals update in real-time as you add, remove, or modify the duration of any teaching step.

2.3. Workflow Visualization
To ensure a logical learning path, the tool draws connections between objectives.

Connecting Lines: A clear, visual workflow map with dashed lines and arrows connects the objectives within each module.

Sequence Mapping: This helps you visualize the instructional sequence and identify any potential gaps or illogical progressions for learners. The map automatically updates whenever objectives are reordered.

2.4. Automated Change Reporting
This feature provides accountability and simplifies communication with leadership.

On-Demand Reports: At any point, click the Generate Change Report button. The tool compares the current state of the curriculum to the state it was in when the page was first loaded.

Detailed Summaries: The report provides a clear, text-based log of all modifications, including:

[+] ADDED: Any new modules, objectives, or steps.

[-] DELETED: Any content that has been removed.

Title changed from...: Records of any renaming.

Total time changed by...: Precise changes in timing for modules and objectives.

Objective flow has changed: A summary of the old vs. new order of objectives.

Clipboard Ready: The report is designed for easy copying and pasting into emails, Word documents, or presentations.

Page 3: Usage Instructions & FAQ
3.1. Getting Started & Basic Operations
Open the File: Simply open the course_design_tool.html file in a modern web browser (Chrome, Firefox, Edge, Safari). The application will load with sample data to demonstrate its functionality.

Edit Content: Click on any title to type. Click on a time field to change the number.

Add Content: Use the + Add buttons at the module, objective, or step level to build out your course.

Delete Content: Use the Delete or ✕ buttons to remove items. Deleting a module will remove all its contents, and a confirmation prompt will appear to prevent accidents.

3.2. Data Management & Persistence
Local Storage: Your work is automatically saved to your browser's local storage. This means the data is stored on the specific computer and in the specific browser you are using.

Persistence: You can safely close the browser tab and reopen it later; your curriculum will be preserved.

Important Limitations:

Data is not automatically shared between different computers or different web browsers (e.g., work done in Chrome will not appear in Firefox).

Clearing your browser's cache or site data will permanently erase your work. For long-term storage, it is recommended to keep a backup of your curriculum plan.

3.3. Frequently Asked Questions (FAQ)
Can I share my curriculum with a colleague?
Not directly through the application. Since data is stored locally, the best way to share is to have them use the tool on their machine or to use the "Generate Change Report" to export a text-based summary of the structure.

Is there an "undo" button?
Currently, there is no undo functionality. Changes like deletions are permanent for the session. However, if you reload the page without making further changes, it will revert to the state it was in when you first opened it.

How do I start a new curriculum from scratch?
To clear all existing data, you can clear the local storage for the site. In most browsers, you can do this by opening the developer tools (F12), going to the "Application" tab, selecting "Local Storage," and deleting the relevant key associated with the file.

Can I export my work to a file?
The application does not have a file export feature. The best way to create a distributable copy of your work is to use the Generate Change Report feature at the end of a session and save the text output in a separate document.

What happens if the application is updated?
Since this is a single HTML file, "updating" it means replacing it with a new version. This action should not affect your locally stored data as long as the domain/path remains the same. However, it is always a good practice to back up your report data before switching to a new version.

Page 4: Advanced Topics & Technical Info
4.1. Best Practices for Curriculum Management
Session-Based Changes: Think of your work in sessions. Open the tool, make a series of related changes, generate a change report, and then save that report externally. This creates a historical log of your design decisions.

Backup Your Data: Since data is stored locally in the browser, it's vulnerable to being cleared. Periodically, copy the entire content of the Change Report and paste it into a text file or official document as a backup of your curriculum structure.

Managing Large Courses: For very large or complex courses, consider breaking them down into separate major parts and managing them in separate sessions to keep the visual board clean and responsive.

4.2. Troubleshooting
My data has disappeared!
This is almost always caused by clearing browser data/cache. Unfortunately, if the local storage has been cleared, the data cannot be recovered through the tool. This highlights the importance of regular backups using the report feature.

Drag-and-Drop is not working.
This feature should work in all modern web browsers. If you are having issues, ensure you are using an up-to-date version of Chrome, Firefox, Edge, or Safari. If the problem persists, try disabling browser extensions that might interfere with JavaScript execution.

The workflow lines look misaligned.
The lines are drawn automatically based on the position of the objectives. If they appear misaligned, a simple page refresh will usually force them to redraw correctly.

4.3. Technical Details
Platform: This is a standalone client-side web application. It runs entirely in your web browser and does not require an internet connection after the initial file is loaded.

Technology Stack:

HTML: For the core structure.

Tailwind CSS: For modern styling and a responsive layout.

JavaScript: For all application logic, including drag-and-drop, time calculations, and report generation.

Data Storage: All data is stored in the browser's localStorage API, a key-value store that persists across browser sessions.
