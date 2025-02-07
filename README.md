# Date and Time Range Picker

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)  

A user-friendly date and time range picker using jQuery UI Datepicker and Timepicker.  This component allows users to easily select a start and end date/time, with built-in validation and convenience features.

## Demo

[https://ProgrammerNomad.github.io/Date-and-Time-Range-Picker/](https://ProgrammerNomad.github.io/Date-and-Time-Range-Picker/)  

## Features

*   **Intuitive Date Selection:** Utilizes jQuery UI Datepicker for easy start and end date selection.
*   **Precise Time Selection:** Employs the Timepicker plugin for accurate start and end time input.
*   **Robust Date Range Validation:** Prevents users from selecting an end date/time before the start date/time, and vice-versa.  If the start date is changed to be after the current end date, the end date and time are cleared. The same logic applies when the end date is changed to be before the current start date.
*   **Automatic End Datepicker Opening:**  The end datepicker automatically opens after a start date is selected, streamlining the user experience.
*   **Initial Date/Time Defaults:** Sets the initial start date to the current date, start time to 15 minutes from the current time, end date to two days from the current date, and end time to match the start time (or 15 minutes from the current time, if the end date is today).
*   **Restricted Past Dates (Start Date):**  Users cannot select past dates for the start date, ensuring logical date ranges.
*   **Clear Display:** Displays the selected date and time range clearly and concisely.

## Technologies Used

*   HTML
*   CSS
*   JavaScript
*   [jQuery](https://jquery.com/) (v3.7.1 or later)
*   [jQuery UI](https://jqueryui.com/) (v1.13.2 or later)
*   [Timepicker Plugin](https://github.com/jonthornton/jquery-timepicker) (v1.3.5 or later)

## Installation

You can use this date/time picker in your project in a few ways:

1.  **Directly from GitHub Pages (for testing/quick integration):**  Include the necessary CSS and JavaScript files directly from the GitHub Pages demo in your HTML.

    ```html
    <link rel="stylesheet" href="[https://code.jquery.com/ui/1.13.2/themes/base/jquery-ui.css](https://code.jquery.com/ui/1.13.2/themes/base/jquery-ui.css)">
    <link rel="stylesheet" href="[https://cdnjs.cloudflare.com/ajax/libs/timepicker/1.3.5/jquery.timepicker.min.css](https://cdnjs.cloudflare.com/ajax/libs/timepicker/1.3.5/jquery.timepicker.min.css)">

    <script src="[https://code.jquery.com/jquery-3.7.1.min.js](https://code.jquery.com/jquery-3.7.1.min.js)"></script>
    <script src="[https://code.jquery.com/ui/1.13.2/jquery-ui.js](https://code.jquery.com/ui/1.13.2/jquery-ui.js)"></script>
    <script src="[https://cdnjs.cloudflare.com/ajax/libs/timepicker/1.3.5/jquery.timepicker.min.js](https://cdnjs.cloudflare.com/ajax/libs/timepicker/1.3.5/jquery.timepicker.min.js)"></script>

    ```

2.  **Clone the Repository (for development/modification):**

    ```bash
    git clone [https://github.com/ProgrammerNomad/Date-and-Time-Range-Picker.git](https://www.google.com/search?q=https://github.com/ProgrammerNomad/Date-and-Time-Range-Picker.git)
    ```

    Then, copy the necessary files (`index.html` or the relevant JS/CSS) into your project.

## Usage

1.  Include the required CSS and JavaScript files in your HTML (as shown in the Installation section).
2.  Add the HTML structure for the date and time pickers (see `index.html` for an example).
3.  Initialize the datepickers and timepickers using jQuery (see the provided JavaScript code in `index.html`).

```javascript
// Example initialization (adjust selectors as needed)
$(function() {
    $("#startDate").datepicker({ /*... options... */ });
    $("#startTime").timepicker({ /*... options... */ });
    //... initialize other pickers
});