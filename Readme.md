# Freight Incident Analysis Tool (FIAT)

## Introduction

This documentation provides an overview of the Hazard Spill Simulation Tool, a custom ArcGIS Pro tool designed to simulate chemical spills. The tool reads a CSV file with specific columns and outputs a point layer with a buffer around each point, representing the potential area affected by a chemical spill.
Requirements:

    ArcGIS Pro (latest version recommended)
    The provided Hazard Spill Simulation Tool package (zipped folder)

## Developers
D. Blassingame - GIS Major Undergraduate | The Ohio State University
R. Brown - GIS Major Undergraduate | The Ohio State University

## Limitations

Due to the complex nature of chemical spills and hazardous we have excluded the affected population by chemical and have left the manual buffer radius for the chemicals in (miles) units.

Developers are implementing a way to use Python RegEx as an ETL process to cleanse data, this feature will be released on future versions located at: https://github.com/djbosu/RRAnalysis

## DATA Preparation

    To use your own data with the Hazard Spill Simulation Tool, ensure your CSV file includes the following columns, casing and spelling are critical for a successful run of the tool. Proper column headers are capitalized here.

        LONGITUDE: The longitude coordinates of each point.
        LATITUDE: The latitude coordinates of each point.
        CARSHZD: A column indicating whether a spill is hazardous (1) or non-hazardous (0).
        NARR2: (sometimes Narr1-6 or just narrative): Type of spill
        PERSONS_EVACUATED: Amount of local population

## Installation

    Download the Hazard Spill Simulation Tool package (zipped folder) and unzip the contents to a desired location on your computer.
    Open ArcGIS Pro and create a new project.
    In the Catalog pane, right-click on the "Toolboxes" folder, and select "Add Toolbox".
    Navigate to the unzipped folder containing the Hazard Spill Simulation Tool, and select the toolbox file to add it to the project.
    Add the provided data (CSV file) to the project folder.

## Usage

    Open the Hazard Spill Simulation Tool from the Catalog pane.
    Fill out the parameters in the tool dialog:
        Workspace: Set the workspace folder where the output data will be stored.
        Source File: Browse to the CSV file containing the input data (must have LONGITUDE, LATITUDE, and optional CARSHZD columns).
        Buffer Radius: Enter the buffer radius (in map units) to be applied around each point.
        Hazard Spill (optional): Select a hazardous material from the dropdown list, or enter a custom value if the desired material is not listed.
        Output Layer: Enter a name for the output layer.
    Click "Run" to execute the tool.

The tool will create a point layer with a buffer based on the entered buffer radius, simulating a chemical spill. The output will be added to the ArcGIS Pro map.

## Future Enhancements

The next version of the Hazard Spill Simulation Tool will include pre-determined buffer radii and allow users to simulate chemical spills based on the selected hazardous material.

## Troubleshooting

If you encounter any issues while using the Hazard Spill Simulation Tool, refer to the following troubleshooting tips:

    Verify that your input CSV file contains the required columns (LONGITUDE, LATITUDE, and optional CARSHZD) and that the column names are spelled correctly and in uppercase.

    Ensure that the buffer radius entered is a valid positive number and in the correct unit of measurement.

    Double-check that the ArcGIS Pro project and the Hazard Spill Simulation Tool are using the same spatial reference system. Coordinate system mismatches can cause unexpected results or errors.

    If an error occurs during the tool execution, review the error message and traceback for specific details about the issue. If necessary, consult ArcGIS Pro documentation or online forums for further guidance.

    If the tool does not produce the expected output, verify that the input parameters have been entered correctly and that the input data is properly formatted.

## Support and Feedback

If you need further assistance or would like to provide feedback about the Hazard Spill Simulation Tool, please contact the developer at https://github.com/djbosu/RRAnalysis

## Disclaimer

The Hazard Spill Simulation Tool is provided "as is" without any warranty, express or implied. The developer is not responsible for any direct, indirect, or consequential damages resulting from the use of the tool. Users are responsible for ensuring the accuracy and validity of their data and are encouraged to verify the results obtained from the tool using independent sources. The tool is intended for educational and demonstration purposes only and should not be used for making real-life decisions related to hazardous materials or emergency response.
