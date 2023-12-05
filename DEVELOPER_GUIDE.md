# Developer Guide for MAJOR SELECT SYSTEM

## Overview

The "MAJOR SELECT SYSTEM" is a graphical user interface (GUI) application built using the Tkinter library in Python. It allows users to filter and display data from a Pandas DataFrame containing information about educational programs.

The application provides multi-select functionality for filtering data based on various criteria such as institution state, institution, CIP (Classification of Instructional Programs) name, and degree level. Users can also choose specific columns to display in the final results.

## Prerequisites

- Python 3.x
- Pandas library
- Tkinter library (included in standard Python distribution)
- `ttk` module from the Tkinter library

Make sure to install the required libraries before running the application:

```bash
pip install pandas
```

## Running the Application

The main application is defined in the `MainApplication` class. To run the application, execute the script containing the code. For example:

```bash
python your_script_name.py
```

## Application Features

### MultiSelectWindow Class

The `MultiSelectWindow` class is a custom Tkinter Toplevel window that provides a multi-select interface using checkboxes. It is used for selecting multiple values from a list of options.

#### Methods:

- `__init__(self, parent, options, title, callback)`: Constructor for the window.
- `on_canvas_configure(self, canvas, frame)`: Configures the canvas for scrolling.
- `on_frame_configure(self, canvas)`: Configures the frame for scrolling.
- `select_all(self)`: Selects all checkboxes.
- `deselect_all(self)`: Deselects all checkboxes.
- `submit_selection(self, callback)`: Submits the selected values and calls the provided callback function.

### MainApplication Class

The `MainApplication` class is the main GUI application that utilizes the `MultiSelectWindow` class. It provides features for filtering and displaying data based on user selections.

#### Methods:

- `__init__(self)`: Constructor for the main application.
- `show_multi_select(self, options, title, callback)`: Displays the multi-select window for the specified options.
- `reset_selections(self)`: Resets all selections and clears the display.
- `filter_states(self, selected_values)`: Filters data based on selected institution states.
- `filter_institutions(self, selected_values)`: Filters data based on selected institutions.
- `filter_cip_names(self, selected_values)`: Filters data based on selected CIP names.
- `filter_degree_levels(self, selected_values)`: Filters data based on selected degree levels.
- `display_final_results(self)`: Displays the final results in the text widget.
- `show_column_selection(self)`: Shows the multi-select window for choosing columns.

## Usage

1. Run the script to launch the application.
2. Use the "choose institution_state" button to select one or more institution states.
3. Follow the subsequent prompts to filter data based on institutions, CIP names, and degree levels.
4. Use the "choose variables" button to select columns for display.
5. Click the "RESET" button to clear all selections and start over.
6. The final results are displayed in the text widget with horizontal and vertical scrollbars.

