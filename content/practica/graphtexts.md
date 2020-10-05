---
type: practicum
layout: single
title: Download and analyze the texts on your phone.
when: October 7
---

Use them to visualize patterns in the relationship between you and a friend.

<!--more-->

An exercise designed by [Jérémie Lumbroso](https://www.cs.princeton.edu/people/profile/lumbroso), who will join us in class.

## Download

For those of you with Mac hardware, there are three elements you'll need for this practicum: 1) [PhoneView](https://www.ecamm.com/mac/phoneview/) (software used for downloading text messages from your phone as plain text, CSV files on your laptop), 2) our visitor Jérémie Lumbroso's code written in Python, and 3) Anaconda for opening and running Jérémie's code. Here are the detailed instructions:

1. Download the full, paid version of PhoneView using the link I shared in our Slack. Open the .zip file and move the program to your Applications folder.
    - If you have any trouble downloading your texts as a CSV file, if you don't have the cable to connect your phone to your laptop, or **if you would prefer not to use personal text messages for this exercise**, feel free to use this sample CSV file adapted from [the all-time greatest TV series](https://www.dropbox.com/s/0nycft7ztwrmr0w/worf.csv?dl=0).
2. Download the code in Jérémie's [GitHub repository](https://github.com/jlumbroso/text-message-analysis-notebook). Click the green "Code ↓" button and select "Download Zip."
    - Once downloaded, open that .zip file to unpack its contents.
3. Download Anaconda, a free, open-source distribution of Python and R. [Click the 'Download' button on this page,](https://www.anaconda.com/products/individual) and for Mac, select "64-Bit Graphical Installer (462 MB)."
    - Once downloaded, double click the installer file `Anaconda3-2020.07-MacOSX-x86_64.pkg`. The installer file will automatically place Anaconda-Navigator in your Applications folder.

## Analyze

### PhoneView

- Open PhoneView from your Applications folder. When a message pops up reading "This is an application downloaded from the internet. Are you sure you want to open it?" click yes. Read and accept license agreement.
- Connect your phone with a USB cable to your laptop. Unlock your phone's screen. You may have to tell your phone that this laptop is a trusted device using an iCloud code sent via text, or by accepting it in a pop up window.
- Data should begin transferring in PhoneView automatically. **All data is stored locally on your computer's hard drive, and nothing will ever be transferred online.**
- Once all text messages have populated the "data" column, select the person whose correspondence you'd like to analyze. Then click the icon on the top left, "Copy From iPhone." Save the CSV file.
- Open the folder you unzipped from Jérémie's GitHub repository, titled `text-message-analysis-notebook-master.` Drag the CSV file containing your text messages into this folder.

### Anaconda

- Open Anaconda-Navigator in your Applications folder. Click the "Launch" icon beneath Jupyter Notebook. This will open a terminal window and a browser window.
- In the localhost window opened in your web browser, navigate to the `text-message-analysis-notebook-master` folder. Click on the file `Text Analysis.ipynb`. This will open a new window.
- In the section of the code with a heading that reads "**Importing the text message data**", change the CSV filename in the following line the filename of your text message CSV. Again, make sure that you've moved that CSV file into the folder you unzipped from GitHub.
    - `df = pvh.load_csv(filepath="text_messages.csv", keep_type=False)`
- Click on that line of code so that it is surrounded by a green box, and typing SHIFT+ENTER. You should see the three most recent texts you sent populate the code.
  - If you receive an error message instead, try adding a new line of code at the very top of this file that reads: `import pandas`
- Continue clicking on each line of the code, and then typing SHIFT+ENTER. The graphs will change to reflect your text messages.

## Notes

- For a detailed introduction to Jupyter Notebooks for digital humanities, use the "[Introduction to Jupyter Notebooks](https://programminghistorian.org/en/lessons/jupyter-notebooks)" tutorial from *The Programming Historian.*