# Pixel Focus OS 🕹️

A retro, pixel-art-themed productivity dashboard to help you focus and get things done. This is a standalone desktop application built with Electron.

!
<img width="1619" height="892" alt="image" src="https://github.com/user-attachments/assets/cca2362b-d007-4887-877d-dbaa11007ec2" />
<img width="784" height="1037" alt="image" src="https://github.com/user-attachments/assets/4558e2c4-d97a-4d0c-8c15-5c1fa5ce004f" />

---

## About The Project

Pixel Focus OS is a simple, all-in-one productivity application designed for offline use. It wraps a feature-rich web interface into a native desktop experience using Electron. The app provides a suite of tools including a Pomodoro timer, task management, goal setting, and progress tracking, all presented in a charming pixel-art style. All your data is saved locally in your browser's `localStorage`.

---

## Features

-   **Pomodoro & Custom Timer:** Use the classic Pomodoro technique with 'Focus', 'Short Break', and 'Long Break' sessions, or set your own custom timer duration.
-   **Task Management:** A daily to-do list that works with a calendar to help you organize tasks for specific dates.
-   **Mission Control (Goals):** Set and track your Daily, Weekly, Monthly, and Yearly goals. Categorize them with tags like 'Health', 'Money', and 'Education'.
-   **Progress Tracker:** Visualize your focus sessions with daily, weekly, and monthly views to see your productivity over time.
-   **Themes & Sounds:** Customize your experience with multiple color themes and toggleable click sound effects (SFX).
-   **Brown Noise Generator:** An integrated ambient noise player with 'Deep', 'Medium', and 'Light' presets to help you concentrate.
-   **Global Progress Bars:** See how much of the day, week, month, and year has passed at a glance.

---

## How It Works

This application has a simple but effective architecture that combines native desktop capabilities with modern web technologies.

* **Electron Main Process:** The core of the desktop application is `main.js`. This script runs in a Node.js environment and is responsible for creating and managing the application's lifecycle and native windows. It creates a `BrowserWindow` instance and loads the `pixel-focus-os.html` file into it.

* **Renderer Process (The UI):** The entire user interface is contained within a single file, `pixel-focus-os.html`. This file runs in a Chromium-based renderer process, separate from the main process.

* **Frontend Framework:** The UI is built using **React**. Instead of a complex build setup, React and ReactDOM are loaded directly via script tags in the HTML file.

* **Real-time JSX Transpilation:** The React components are written in JSX directly within a `<script type="text/babel">` tag. The **Babel** library, also loaded via a script tag, transpiles this JSX into standard JavaScript directly in the browser at runtime.

* **Styling:** Utility-first styling is provided by **Tailwind CSS**, which is configured and executed in the browser through its CDN script.

* **Data Persistence:** All user data—including tasks, goals, progress, and settings—is saved to the browser's `localStorage`. This is managed by a custom React hook (`useLocalStorage`), ensuring that your information persists even after you close and reopen the application.

---

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

You need to have **Node.js** and **npm** (Node Package Manager) installed on your system. You can download them from [nodejs.org](https://nodejs.org/).

### Installation & Running the App

1.  **Clone the repo**
2.  **Navigate to the project directory**
    ```sh
    cd pixel-focus-desktop-app
    ```
3.  **Install NPM packages**
    ```sh
    npm install
    ```
    **Important:** This step is mandatory. The project's dependencies, including the Electron framework itself, are listed in the `package.json` file. These dependencies are stored in a folder called `node_modules`, which is over 200MB in size. This folder is **intentionally not uploaded** to GitHub to keep the repository lightweight. The `npm install` command reads the `package.json` file and downloads all the necessary dependencies for you.

4.  **Run the app**
    ```sh
    npm start
    ```
    This command executes `electron .` as defined in your `package.json`, which starts the Electron application.

---

## License

Distributed under the ISC License. See `package.json` for more information.

---

## Contact

Navaneeth Sankar K P - nave.ethan1337@gmail.com
[LinkedIn](https://www.linkedin.com/in/navaneeth-sankar-k-p)
