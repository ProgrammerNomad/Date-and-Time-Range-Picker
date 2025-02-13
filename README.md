# Date and Time Range Picker

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A user-friendly date and time range picker using jQuery UI Datepicker and Timepicker. This component allows users to select date ranges while automatically handling disabled dates and preventing invalid selections.

## Demo

[https://ProgrammerNomad.github.io/Date-and-Time-Range-Picker/](https://ProgrammerNomad.github.io/Date-and-Time-Range-Picker/)

## Features

* **Smart Date Range Selection:** 
  - Automatically prevents selection of ranges that include disabled dates
  - Intelligently adjusts end date options based on start date selection
  - Supports single-day selection even when next day is disabled

* **Intuitive Interface:**
  - jQuery UI Datepicker for date selection
  - Timepicker plugin for precise time input
  - Automatic validation of date/time ranges

* **Advanced Validation:**
  - Prevents selection of disabled dates
  - Automatically limits end date selection to avoid disabled dates
  - Clears invalid selections when date constraints change

* **Time Management:**
  - 15-minute interval time selection
  - 24-hour time range support
  - Automatic time adjustment based on date selection

* **Default Behaviors:**
  - Sets start date to current date
  - Initializes start time to next 15-minute interval
  - Automatically finds next valid end date
  - Handles time selection across date boundaries

## Technologies Used

* HTML5
* CSS3
* JavaScript (ES6+)
* jQuery v3.7.1
* jQuery UI v1.13.2
* jQuery Timepicker v1.3.5

## Installation

### Quick Start (CDN)
Include the required files in your HTML:

```html
<!-- CSS -->
<link rel="stylesheet" href="https://code.jquery.com/ui/1.13.2/themes/base/jquery-ui.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/timepicker/1.3.5/jquery.timepicker.min.css">

<!-- JavaScript -->
<script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
<script src="https://code.jquery.com/ui/1.13.2/jquery-ui.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/timepicker/1.3.5/jquery.timepicker.min.js"></script>
```

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/ProgrammerNomad/Date-and-Time-Range-Picker.git
```

2. Navigate to the project directory:
```bash
cd Date-and-Time-Range-Picker
```

## Usage

### Basic Implementation

1. Add the HTML structure:
```html
<div class="container">
  <div class="input-group">
    <label for="startDate">Start Date:</label>
    <input type="text" id="startDate" placeholder="Start Date">
  </div>
  <div class="input-group">
    <label for="startTime">Start Time:</label>
    <input type="text" id="startTime" placeholder="Start Time">
  </div>
  <div class="input-group">
    <label for="endDate">End Date:</label>
    <input type="text" id="endDate" placeholder="End Date">
  </div>
  <div class="input-group">
    <label for="endTime">End Time:</label>
    <input type="text" id="endTime" placeholder="End Time">
  </div>
</div>
```

### Configuring Disabled Dates

Define dates that should be unavailable for selection:

```javascript
const disabledDates = ["2025-02-16", "2025-02-18", "2025-02-19", "2025-02-26"];
```

### Getting Selected Date Range

```javascript
function getCombinedDateTime() {
    const startDate = $("#startDate").val();
    const startTime = $("#startTime").val();
    const endDate = $("#endDate").val();
    const endTime = $("#endTime").val();

    return {
        start: startDate + ' ' + startTime,
        end: endDate + ' ' + endTime
    };
}
```

## API Reference

### Key Methods

- `initializeDateTimePickers()`: Initializes the date and time pickers with default values
- `getCombinedDateTime()`: Returns the selected date and time range
- `beforeShowDay()`: Controls date availability in the calendar
- `onSelect()`: Handles date selection validation and updates

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support, please open an issue in the GitHub repository or contact the maintainers.