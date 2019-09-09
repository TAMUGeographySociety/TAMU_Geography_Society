# FME Introduction Course:

### Program: Feature Manipulation Engine (FME)
FME is a software created by Safe Software, a company based out of Canada. FME is a data integration platform with the best support for spatial data worldwide. With FME you can automate your data integration workflows and distribute your data to those who need it so you can spend more time using your data, and less time fighting it.

**-- [Click here to download FME](https://www.safe.com/support/support-resources/fme-downloads/) --**

Make sure you are only installing FME Desktop 2019.1 - 64 bit for 64 bit computers, 32 bit for 32 bit computers.

[How to tell your computer's bit type](https://lmgtfy.com/?q=how+to+tell+if+your+pc+is+64+or+32+bit)

---

#### Get a student licence!!!

You will need a student licence to be able to use this program.

[You can apply for a student license here](https://www.safe.com/fme/fme-desktop/trial-download/) - Choose the Student - Free Licence option

Make sure to do this BEFORE the Workshop begins!

---

**It is IMPORTANT to have ArcGIS (ArcMap or ArcPro) installed on your computer before you install FME** (We will not be using it the first meeting, but in future meeting we may use ArcPy)

After you install, put in your licence in and you're done! If you can pull up FME 2019.1 Workbench then you've successfully installed FME. 

---

Q/A
1. Which version do you recommend?
    * I will be working with the FME 2019 version but if you already have 2018 installed, you will be fine.
2. Do I need a Windows device to use FME?
    * Nope! FME works on Windows, Linux, and Mac operating systems.
3. Do I need to know how to code to take this course?
    * No coding knowledge is needed to use FME
4. I have another question!
    * Email us at thetamugeographysoceity@gmail.com

## Data:
We will be using a CSV file to start us off that contains some wellbore data.

[Click here to download the CSV file](https://raw.githubusercontent.com/TAMUGeographySociety/TAMU_Geography_Society/master/Learning/Week1/BorestickData.csv)

Hit Ctrl+S on the page and save it to your computer ... or I will show a way to scrape it directly from the internet during the lesson.

## What we are doing:
During this first course I will be teaching the basics of FME and how to use it. I will be using an example of something I did this summer at my time in the oil and gas industry that is simple enough for a beginner level understanding of the program. Those that are advanced in FME may still benifit from coming as they will get experience with oil and gas and FME processes.

If you have any questions about content, location, time, or other ... email me at **thetamugeographysociety@gmail.com**


# Walkthrough:
#### This walkthrough currently does not include pictures, only text. For instructors that want images email liamlyle@tamu.edu about potentially making a class/lesson out of this walkthrough.

0. Lets download our data before we start.
   - Look in the about section titled "Data" and follow those instructions
1. Open FME Workbench 2019 (Versioning dosen't matter between 2019.0, 2019.1 ... etc)
2. Hit 'New' for a new Workspace
3. Lets talk about reading:
   - FME is a program that reads a plethora of data types. You can read all these data types (CSV, SHP, GDB, DWG ...) into your workspace and FME will put the data into a common-data type that works within the FME atmosphere.
   - To create a reader, click the **Reader Button**. This is on your taskbar and the top of the screen and it looks like a cylinder with an arrow pointing to the right.
4. The Reader:
   - We will be reading the CSV data that we downloaded at 
