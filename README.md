# ssotme-ms-airtable-ionic-sassymq-seed
An Ionic Sassy Seed based on an Airtable.com base.

#### Full [Airtable.com](https://Airtable.com) Roadmap
For a full project roadmap, use: 
 - [Roadmap Airtable Template](https://airtable.com/shriiZMSnMwtOUKY3)

Includes:
 - Roadmap - Project Phases/Budget
 - User Stories
 - Actors
 - Lexicon - API
 - Entities - things
 - App States
 - Settings

Or, for an empty starting project, use: 
 - [An Empty Airtable Template](https://airtable.com/shrGgWOuXXxhZls1c)

#### Other [Airtable.com](https://Airtable.com) Starter Templates:
- [IMDB like Template](https://airtable.com/shrBjd3rF6J9oB2Wx)
- [Simple Company Template](https://airtable.com/shr12ryYJilZGEZuj)
- [Piano Service Template](https://airtable.com/shrUU5nLreXumAQHK)
- [Simple Task Manager](https://airtable.com/shrLrXduwAKlsI3bS)
- [Party Games Template](https://airtable.com/shrpcXNi5Iq2mh1mN)
- [Homework Plus Template](https://airtable.com/shrOxjT36OAKciofE)

# Using this Seed:

### Create an [Airtable.com](https://Airtable.com) Base

Airtable.com is *by far* the best tool I've found (so far) for describing a Single Source of Truth. 
It has all the flexibility of a Spreadsheet + the formal structure of a Database.

There are a list of starter templates above.  You can either pick one of the example templates
above, or start with an Empty template and build your own.  

4. Generate an API key on your account

   * If you have not already created an API Key - this is how to do it.
   * Close the airtable to get to the Airtable.com home page.
   * Click on your account icon in the top right corner of the screen and choose "Account"
   * Scroll down and click "Generate Key" to create an API key

2. Copy API Key from Acount Page

3. Configure [Airtable.com](https://Airtable.com) API Key in the SSoT.me CLI.
   - This key is passed along with any requests sent to the airtable account tools.
   - At a command line, type `>ssotme -setAccountAPIKey airtable=YOUR_AIRTABLE_API_KEY`


1. Find an Airtable Template above to start with

   * Open one of the airtables above and Click *copy base* in the top right corner to create a 
copy in your own Airtable.com account.

4. Customize the Airtable

   * Just follow the patterns established.  Add as many sheets of data as you want, and simply list 
each sheet on the "Entities" tab.  That's the only "rule".


5. Copy BaseID

   * Open the API Documentation from the Help Menu in the top right corner.
   - https://api.airtable.com/v0/{THIS_IS_THE_BASE_ID}/TableName
   - The `Base ID` will start `app...`

### Fork and Clone this Repo

1. Fork and Clone this repo

   * Click Fork in the top right corner of Github

2. Rename the copy created in your account.

   * Rename the repo on the settings tab.

3. Clone the repo

   * Clone the repo to a folder on your local computer.

5. Add Base ID and API key from Above.

   * Update the "SSoTmeProject.json" file with the Base ID you copied above
   * This is the line in the original Seed:
        `"CommandLine": "airtable/airtable-to-xml -p baseId=BASE_ID_HERE"`


6. Make sure you have the latest SSoT.me CLI tools installed.

6. Run the `ssotme -init`

   * Open a powershell prompt in the repo root folder, and type `>ssotme -init`.  
The name of the project will be inferred from the name of the folder.

   - *NOTE* - if the `Base ID` OR `API KEY` is wrong - it will be reported right away in the 
 init process as a 404 error on Airtable.

   - Also - if the `AirtableName` values for any enties included do not match a tab in your Airtable, 
 the SSoT.me CLI will complain and tell you which entity does not match.

8. Download Packages & Build Ionic Mobile App

   * Execute `/ionic-ts-sidemenu/>prepare-ionic.bat` to start the ionic project downloading 
        npm packages and building the mobile app.

1. Create Sql Server DB

     * Run the `/SqlServer/UpdateSchema.sql` to create (or update the schema for) a SQL Server Database.

7. Open Visual Studio
     * Open the Visual Studio Solution (.sln) file that will be in the project root folder.

9. Include additional project files

     - In visual studio open `/Windows/CoreLibrary/SassyMQ/` and include the 3 `.cs` 
files which are not automatically included.

    - In the visual studio project, open `/MVCRestAPI/Controllers/` and include the `api/*Controller.cs` 
rest api controllers which are not automatically included in the project when detected.

### Run the project

11. Make the `MVCRestAPI` the startup project in the solution.

12. Press F5 to run the project.  This will start the REST API.

13. in powershell, run `ionic-ts-sidemenu/>ionic serve` to start the Ionic Mobile app.  

### Et Voila! 

"Spreadsheet" to mobile app in less than 10 minutes.


