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
   - The window that just popped up is the Reader, it contains a Format, and a Dataset, and a Coord. System.
   - Format is the type of file you are reading in (CSV, SHP, DWG, OBJ ...)
   - The Dataset is the location of that file type you want to add to your workbench
   - Lets go ahead and fill out the information requested:
   - Format should be a **CSV (Comma Seperated Value)** - You can either type this in, or hit the dropdown arrow to the left and search for it.
   - Dataset should be that CSV we downloaded (Hit the tripple dot and find where-ever you saved that CSV at. If you didn't download that CSV, check part 0)
5. Once you've filled in your Format and Dataset information, hit OK (we will get to Coord. System later) ...
   - What you see now is a yellow box that says CSV 
6. Lets Run It!
   - But before we run it, lets talk about feature caching ... Feature Cacheing is a powerful tool in FME. It allows for a user to run a program to a point, and the results will be cached into your computer (APPDATA/TEMP folder by default I think). Once you close FME, this ran data will disapear. The power of this tool is not having to write out a million _test_ files (such as Model Builder and Python). Feature Caching does slow down your process though, so be aware if you are using a lot of data it might be wise to turn it off.
   - Lets turn on feature cashing! In the taskbar ... Run -> Enable Feature Cashing
   - Lets now run our workbench! (You can do this by hitting the Green Run Arrow, or pressing F5 if using a PC ... IDK what it is for Macs)
   - A translation log popped up at our bottom. This will be a very important tool later for debugging, but we will talk about it later.
7. Let talk about the Feature Inspector.
   - FME Workbench is the "running" space, but we need to view this data that we are working with. This viewing application is called the FME Inspector ... where we inspect our data (duh ...)
   - Lets inspect that CSV that we just read in! Click on the CSV and hit the "View Data Source" It looks like a magnifying glass and a cylinder
   - This should pop up the FME Data Inspector - 2019.X window. We have now got a table of data we can work with. Yay!!!
8. Lets go back to our workbench and talk about **Transformers**
   - We've got a table of data now. Lets do something with it. Lets talk about Transformers!
   - We want to _transform_ or change our data. We will do this buy adding a transformer.
   - Our first Transformer to add is an AttributeManager
   - To add a transformer just start typing!
   - Type in the word Attribute and the transformer _Attribute Manager_ should pop up. Click on it!
9. **Connections**
   - Lets talk about how easy FME is. To connect Readers to transformers, all you gotta do is click the little arrow on the right side of our CSV Reader, and pop it into the left side of our attribute manager and we are done! You've connected your first Transformer!!
10. Open the Attribute Manager:
   - Lets go into our attribute manager (you can do this by double clicking on it)
   - These attributes should look familiar to the ones we say back in step 7.
   - Lets do a little bit of data cleaning so we can work with only pertinent data
   - Lets change that "W" (Westing) to the word "E" (Easting) and make it look like N (ft). All you gotta do is type in the text: E (ft) into the Output Attribute column! Boom you've renamed an attribute!
   - We only want to keep these attributes, see if you can figure out how to remove other attributes (hint, look in Actions):

| Keep these attributes |
| --------------------- |
| Measurement Index |
| Inclination (deg) |
| True Vertical Depth (ft) |
| N (ft) |
| W (ft) |

11. Lets spatialize this data!
   - Add a VertexCreator transformer
   - Our X is W (ft)
   - Our Y is N (ft)
   - Our Z is True Vertical Depth (ft) _Make sure you put it as a negitive value_
   - Run your workspace!
   - Lets Inspect your VertexCreator (Green box with Magnifying glass)

12. Add a LineBuilder Transfomer
   - This will make a line of your data
13. Add in an Offsetter:
   - We will be using this to set this well in a location. Use the two coordniates bellow for your offsets:
#### Cords for Offset:
X: 3553465.1633
>
Y: 10210975.9487

14. **TBD** - Let liam know if you want to continue on with this walkthrough
>
>
>
#### If you have any questions, let Liam know by emailing him at liamlyle@tamu.edu
