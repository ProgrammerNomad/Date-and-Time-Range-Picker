# Date and Time Range Picker

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A user-friendly date and time range picker using jQuery UI Datepicker and Timepicker. This component allows users to easily select a start and end date/time, with built-in validation, convenience features, and the ability to disable specific dates.

## Demo

[https://ProgrammerNomad.github.io/Date-and-Time-Range-Picker/](https://ProgrammerNomad.github.io/Date-and-Time-Range-Picker/)

## Features

*   **Intuitive Date Selection:** Uses jQuery UI Datepicker for easy start and end date selection.
*   **Precise Time Selection:** Employs the Timepicker plugin for accurate start and end time input.
*   **Robust Date Range Validation:** Prevents users from selecting an end date/time before the start date/time, and vice-versa.  If the start date is changed to be after the current end date, the end date and time are cleared. The same logic applies when the end date is changed to be before the current start date.
*   **Automatic End Datepicker Opening:** The end datepicker automatically opens after a start date is selected, streamlining the user experience.
*   **Initial Date/Time Defaults:** Sets the initial start date to the current date, start time to 15 minutes from the current time, end date to two days from the current date, and end time to match the start time (or 15 minutes from the current time, if the end date is today).
*   **Restricted Past Dates (Start Date):** Users cannot select past dates for the start date, ensuring logical date ranges.
*   **Disable Specific Dates:** Allows you to disable specific dates in both the start and end date pickers using an array of dates.
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

1.  **Directly from GitHub Pages (for testing/quick integration):** Include the necessary CSS and JavaScript files directly from the GitHub Pages demo in your HTML.  (See the HTML source of the demo page for the exact links.)

2.  **Clone the Repository (for development/modification):**

    ```bash
    git clone https://github.com/ProgrammerNomad/Date-and-Time-Range-Picker.git
    ```

    Then, copy the necessary files (`index.html` or the relevant JS/CSS) into your project.

## Usage

1.  Include the required CSS and JavaScript files in your HTML (as shown in the Installation section).
2.  Add the HTML structure for the date and time pickers (see `index.html` for an example).
3.  Initialize the datepickers and timepickers using jQuery (see the provided JavaScript code in `index.html`).

**Disabling Specific Dates:**

To disable specific dates, modify the `disabledDates` array in the JavaScript code.  The dates should be in `YYYY-MM-DD` format.

```javascript
const disabledDates = ["2025-02-20", "2025-02-15", "2025-02-18"]; // Example disabled dates
```

Refer to the `index.html` file in the repository for a complete working example.

## Contributing

Contributions are welcome! Please feel free to open issues or submit pull requests.

## Need Help?

If you have any questions or need assistance using this date and time range picker, please don't hesitate to open an issue on the repository.  We'll be happy to help!

## License

MIT License