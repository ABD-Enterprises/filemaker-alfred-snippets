# Installation Guide

Follow these steps to install the FileMaker Alfred Snippets collection.

## Prerequisites
- macOS
- [Alfred](https://www.alfredapp.com/) installed
- **Alfred Powerpack** purchased and activated (required for Snippets functionality)

## Steps

1. **Download the Snippets File:**
   Download the `.alfredsnippets` file from the root of this repository:
   - [FileMaker_Functions.alfredsnippets](../FileMaker_Functions.alfredsnippets)

2. **Import into Alfred:**
   Double-click the downloaded `FileMaker_Functions.alfredsnippets` file. Alfred will prompt you to import the snippet collection. Confirm the import.

3. **Verify Snippets are Enabled:**
   - Open Alfred Preferences.
   - Go to **Features** > **Snippets**.
   - Make sure the checkbox next to "Automatically expand snippets by keyword" is **checked**.

4. **Test with a Trigger:**
   Open any text editor or a FileMaker Calculation dialog, and type one of the triggers, for example:
   `;fmlet`
   
   If everything is set up correctly, the text should immediately expand into a `Let ( [] ; )` statement.
