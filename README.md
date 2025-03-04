# BCFA - Blueprint File Analyzer

This is the BCFA (Blueprint File Analyzer) application for macOS designed by Pan Shahbazian (Lotus Labs). It is designed to analyze a set of blueprint files (in JSON format) and generate a report on all custom fields it locates, their occurrences (across the files and where they occur within the modules), and all (if any) shared custom fields.

## Installation

To use the app, simply download the `.zip` file from the [Releases](https://github.com/PanShahbazian/BCFA/releases) section and open it on your Mac.

**Note:** This application requires a directory containing your blueprint files in JSON format to analyze.

### Opening the App for the First Time

If this is your first time opening the app, you might encounter a security warning from macOS' Gatekeeper, especially if the app is from an unidentified developer. Here's how to bypass it:

1. **Right-click** (or **Control-click**) on the `.app` file.
2. Select **Open** from the context menu.
3. A prompt will appear asking if you're sure you want to open the app. Click **Open**.

Once you've opened the app once, you should be able to double-click it in the future to launch it directly.

### Running the App from the Terminal (Optional)

If you'd like to run the app using the Terminal, you can do so with the following command:

    open /path/to/your/app/BCFA.app

For example, if the app is in your Applications folder, you would use:

    open /Applications/BCFA.app

### Permissions

If the app doesn't open, make sure that you have the correct permissions:

Right-click on the `.app` file and select **Get Info**.  
Under **Sharing & Permissions**, ensure that you have **read & write access**.  
If you're still having trouble, check macOS security settings or follow the steps in the **Opening the App for the First Time** section.

## Usage Instructions

### Select Your Blueprint Directory

Upon launching the app, you will be prompted to select a folder containing the JSON blueprint files you wish to analyze. Please make sure your blueprint files are in this folder.

### Name Your Output File

After selecting the directory, the application will ask you what you would like to name the output file.

**Important:** Please do not save the output file in the same directory that contains the blueprint files.

### Processing and Completion

The application will process the files and create a text report. This report will contain the following:

- **Total number of JSON files read.**
- **List of all custom fields in the JSON files.**
- **Occurrences of custom fields:**
  - The module in which the field occurs.
  - How many times the field occurs.
  - Which JSON file contains the field.
- **Fields shared across multiple files.**

### Finishing the Process

Once the analysis is complete, the app will ask if you'd like to analyze another set of files.  
If you wish to analyze more files, click **Yes**.  
If you're finished, click **No** to exit the application.

## Troubleshooting

If the app does not run or you encounter issues:

- **Check Permissions**: Ensure that the `.app` file has proper permissions to run. You may need to go to **System Preferences > Security & Privacy > Privacy** to allow apps from identified developers.
- **Correct File Path**: Make sure the directory you select contains valid JSON files and that you're not saving the output file in the same directory.
- **macOS Version**: This app is designed to run on macOS. Make sure you are using a compatible macOS version.
- Please submit any bug reports or feature requests via the [Issues](https://github.com/PanShahbazian/BCFA/issues) tab.
