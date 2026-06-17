## Alternate-Day Fasting Tracker

A simple, fast, and private web application to track Alternate-Day Fasting (ADF) sessions. Log start and end times, record your weight, monitor BMI automatically, and watch your progress with interactive charts.

<img width="1440" height="816" alt="adfts" src="https://github.com/user-attachments/assets/0d05adb1-281f-471e-8b5e-d2808e5c7935" />

This project is a single HTML file — open it in any modern browser and start tracking immediately. All data is saved locally in your browser.

## Features

    Progress Overview: Live cards for Start Weight, Target Weight, Current Weight, and percentage progress toward goal
    Goal Settings: Configure start weight, target weight, and height (meters) for accurate BMI calculation
    Session Logging: Add fasting sessions with custom date and time pickers (dd/mm/yyyy format)
    Automatic Calculations:
        Duration in hours
        BMI = weight / height²
        Day of week
    Data Table: Sortable log of all sessions with delete option
    Interactive Charts: Built with Chart.js
        Weight over time
        BMI over time
        Fasting duration per session
    Data Management:
        Export all data to JSON
        Import from previous export
        Clear all data with confirmation
    Persistence: Automatic save to localStorage, including collapsed section states
    Responsive UI: Clean gradient design, works on desktop and mobile
    Privacy First: No server, no tracking, no external database

## Demo

    Download index.html and favicon.png (or favicon.svg)
    Double-click index.html to open in Chrome, Firefox, Edge, or Safari
    Start logging

## Getting Started

Option 1: Run locally

bash

git clone https://github.com/yourusername/adf-tracker.git
cd adf-tracker
open index.html

Option 2: Host on GitHub Pages

    Push index.html to your repository
    Go to Settings > Pages
    Select branch main and folder /root
    Your app will be live at https://yourusername.github.io/adf-tracker/

No build step or dependencies required. Chart.js is loaded via CDN.

## How to Use

    Set your goals: Enter Start Weight, Target Weight, and Height, then click "Update Settings"
    Log a session: Enter Date Start, Time Start, Date End, Time End, and your weight, then click "Add Session"
    Review: The table shows duration and BMI automatically
    Visualize: Scroll to Progress Charts to see trends
    Backup: Use "Export Data" regularly to download a JSON backup

## Data Storage

    All data is stored in localStorage under the key fastingTrackerData
    Data never leaves your device
    Clearing browser data will delete your logs — use Export to backup

## File format for export:

    {
      "sessions": [
        {
          "id": 1710000000000,
          "dateStart": "15/06/2026",
          "timeStart": "20:00",
          "dateEnd": "16/06/2026",
          "timeEnd": "20:00",
          "day": "Monday",
          "duration": 24,
          "weight": 78.5,
          "bmi": "25.6"
        }
      ],
      "startWeight": 80,
      "targetWeight": 70,
      "height": 1.75,
      "exportedAt": "2026-06-17T..."
    }

## Tech Stack

    HTML5, CSS3, Vanilla JavaScript
    Chart.js 3.9.1 (via CDN)
    No frameworks, no build tools

## File Structure

    /
    ├── index.html          # Complete application
    ├── favicon.png         # App icon (blue-purple gradient)
    ├── favicon.svg         # Optional SVG icon reference
    └── README.md

## Customization

    Change default values: edit startWeight, targetWeight, and height variables at the top of the script (lines ∼585-587)
    Change colors: modify the gradient #667eea to #764ba2 in the CSS
    Change units: the app currently uses kg and meters

## Browser Compatibility

Tested on latest Chrome, Firefox, Safari, Edge. Requires JavaScript enabled.

## License

MIT License — free to use, modify, and distribute.

## Disclaimer

This app is for personal tracking purposes only. It does not provide medical advice. Consult a healthcare professional before starting any fasting regimen.
