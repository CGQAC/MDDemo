# RPA Week 6 Day 3
## Overview


Microsoft Excel is a very common application used in all remits of business. Dueto its capabilities and popularity, individual components have been built withinUiPath to interact with Microsoft Excel.
![](media/ebc659f1f186bad1e2d3fd4da6576645.png)
To perform any action with an Excel application, the Excel Application ScopeActivity must be used, and all subsequent Activities to be placed within.
The target excel document can be accessed from the triple dot (…) button fromthe Excel Application Scope Activity, with the default path being relative tothe project’s location. This value can be parameterised.
![](media/dbf7ce737daddcb150f0051c8f740fbf.png)
![](media/94657239e07c4823b190660054b8baed.png)
If the file does not exist, one will be created at the given location, with thegiven name, if the CreateNewFile option is checked (it is checked by default).The user is also able to allow or disallow macros from the options too.
The automation can execute Excel activities in the background, if the VisibleOption is unchecked.
The Visible Property option defines whether UiPath will read the file usingMicrosoft Excel (checked), or to perform the read operation internally, directlyon the file (unchecked). UiPath is able to interact with a Microsoft Excel .xlsxfile irrespective of whether the desktop environment has Excel installed or not.
Visible = True (Using Excel):
-   Requires Microsoft Excel to be installed
-   Multiple processes can use the same file concurrently
-   Visible, real-time changes can be observed
Visible = False (Using Direct/Native UiPath):
-   Does not require Microsoft Excel to be installed
-   Only one process can access the file at a time
-   Only works with .xlsx files
-   Can execute as a background activity
Consider the Excel data.
![](media/31c24e5e0f54aafc6c7dd873b7e3d169.png)
Accessing the data from UiPath requires a Read Range Activity. There are twoentry fields for this activity, the SheetName and the Range – by default the“Sheet1” is used for the sheet name and double quotes is used for the range. Thedouble quotes tells UiPath to capture all data within the sheet provided.Alternatively, the user can specify a range similar to Visual Basic notation,
![](media/cedd5602d0a1bf82386de89433fd5683.png)
This activity must have an output variable of type DataTable. Headers can beincluded or ignored with the AddHeaders option.
![](media/c9c4f7daf4effa820c2a5c4477db0a72.png)
Now that the Read Range Activity has an output variable, that variable must beconverted to a string to be able to display the resulting data capture in aWrite Line Activity. The output for the Read Range Activity should be the inputfor the Output Data Table Activity, and the output for the Output Data TableActivity should be a new string variable.
![](media/68e6dc49887cd3e1165a6ce1ad52c687.png)
![](media/50e5e1d9025ca0bc16e4105e2971758f.png)
![](media/b4899e9638f20979cb5ef80935721c82.png)
The Write Range Activity works in almost the same way as the Read RangeActivity, with the exception of needing to supply a valid DataTable variable tothe Activity. In the example below, the Excel Application Scope is a differentone from the Read Range Activity. This is because each Excel document beingworked on requires their own Excel Activity Scope for UiPath to be able tointeract with it. If the file already exists and has data within it, UiPath willunbiasedly write the data over the existing data, with the DataTable datasupplied to the Write Range Activity.
![](media/5ed47b406fc816e0633930a3ce803e71.png)
Append Range works similar to the Write Range Activity, with the exception thatit will add the data ## after##  all the currently existing data, and ## notunbiasedly overwrite.
![](media/f4b5b43f87c85cfcd4a809b0b4174adb.png)
DataTables are a concept within UiPath that work in similar ways to databasetechnologies. Tables can be built, joined, filtered and more. All DataTableActivities can be found under Available -\> Programming -\> DataTable.
![](media/21e8724b1ada097a82bbb378196b6841.png)
Using the Build Data Table Activity, the user is able to create a database-liketable from within UiPath.
![](media/15cce03e375884e24eaa22e28232fdcc.png)
Clicking the DataTable… button, a new dialogue will appear allowing the user toadd or delete rows and columns, as well as edit the column names and row data.
![](media/9ca61dd8a7232e88f33b98a271db0050.png)
If the user requires a new column, clicking the Plus (+) symbol on the top lefthand corner will present a new display, allowing the user to specify the ColumnName, whether the value is allowed to be Null, the Default Value, if the valueshould be Unique, and a Max Length. If the user sets a Max Length of -1 (bydefault), there is no limit to the number of characters for that field.Furthermore, the user must specify the Data Type for the column. If the DataType is a Int32, the user is able to select whether that value must AutoIncrement, perfect for maintaining unique identifiers for the stored data.
![](media/b854df741cd25d67a3dfff9707469084.png)
Please note, that if Auto Increment has been selected for an Int32 value, aDefault Value cannot be supplied. The same is true if Unique value has beenchecked.
If the Data Type required is not visible on the drop down menu, the user mayBrowse for Types ….
Please note, that all VB .NET variable types can be used.
![](media/4a408fe2d2f930c117c4318a323e416b.png)
The user is able to reorder the Columns by click, hold and dragging the columnleft or right.
![](media/c500ce7d092a5bf87534e5d58b97babf.png)
The Build Data Activity must have a DataTable variable to output to.
![](media/10d1c1520dca4b1b5239ebdbedbae5b6.png)
Continuing with the Excel example data above (depicted again below).
![](media/31c24e5e0f54aafc6c7dd873b7e3d169.png)
![](media/b4899e9638f20979cb5ef80935721c82.png)
Following the above Excel Application Scope Activity a Build Data Table Activitywill be used to create some new data. Following this, a Write Range will writethe data of the original Excel data, and then append the new Build Data TableDataTable Output.
![](media/40d383b586bb98ff9cac91d98e4c4d76.png)
![](media/36b8bfbdb8327ff0713be0635a7af1e4.png)
The final output for the Results.xlsx should look like:
![](media/67f1cd38feadfde73077d218ba15c09e.png)
The Sort Data Table Activity allows the user to organise the dataalphanumerically, in ascending or descending order, and can be done on theColumn (which requires a Column Data Type), or more frequently used with anIndex (zero bound) or with robustness in mind, the Name of the column, as itdoes not matter where in the columns index that specific column sits.
The Sort Data Table Activity requires an Input DataTable type and an OutputDataTable type. The Input and Output DataTable can be the same variable.
![](media/b6cc1ebcde4c26724d7d5d7b558f6064.png)
The resulting output should now look like the following.
![](media/3094d24f19b2f65a15068b19f30de4ae.png)
Read Cell Activity reads a specific cell within the target Excel document.
![](media/2d66ec3b4bcafa0f0e7d6d1adad3cc78.png)
Write Cell Activity places data in to the specified cell within the target Exceldocument.
![](media/d885bb46677c38c417ae2766135cf5c9.png)
The Select Range Activity quite simply highlights the specified range. Thisactivity does not achieve anything beyond highlighting the desired cells, and isintended for further processing to be achieved (deleting, copying, moving etc).
![](media/21144129f3c5483e272960a872b25386.png)
Consider the following Build Data Table Activities, taking note of the datawithin the ID fields in both activities.
![](media/2a946cd2538cf96153211ea2281b2754.png)
![](media/2b9f4b913dfe1d06e270ceb30528fd44.png)
Using a Join Data Tables Activity, the user is able to combine the twoDataTables (in this instance, two was built within UiPath in oppose to scrapingthe data from an Excel document) based on a number of requirements.
![](media/08af69d4a3a395ec8459bae9cf90ab19.png)
The types of joins that can be achieved are:
-   Inner Join - Select all records from Table A and Table B for which the joincondition is met. All rows that do not match are removed from the resultingtable
-   Left Join - The left join selects records from the first (left-most) tablewith matching right table records. Null values will be inserted into thecolumns for the rows from A that do not have a match in the rows in B
-   Full Join - Used to select all records that match either left or right tablerecords. Null values will be added into the rows from both tables that donot have a match.
![](media/c709f817c00911d0e683d141921bdf33.png)
![](media/a7e80b36866ef44e3806c17bc0496b62.png)
Once the user selects the Join Wizard… button a new dialogue box will presentitself. Input DataTable 1 and 2 must be filled with a DataTable variable, andthe Join Type will need to be changed from the default Inner if another type isrequired. An Output DataTable variable must also be supplied.
Finally, the columns to join on must be provided – as the name of the column forboth DataTables in this instance are called ID, a match will be made over thatfield as depicted below.
If the user requires more columns to make joins with, the plus (+) button on thefar right can be used to add additional conditions.
The result of an Inner Join.
![](media/a815a54ea6b3dd46d31d23b0873ec9a5.png)
The result of a Left Join. Please note the additional data with NULL fields.
![](media/2b8241624d96917a8b21a853d005d3c5.png)
The result of an Full Join. Please note the additional data with NULL fields.
![](media/5c76d66b95b134350d88dc12881a48d7.png)
A Filter Data Table Activity allows the user to Keep or Remove data that matchesa specific criteria. The user must suply an Input DataTable and an OutputDataTable. Again, these DataTable variables for input and output can be the samevariable.
Multiple conditions can be set with the AND or the OR operator on the left handside, after adding another condition with the plus (+) button on the right handside of the condition(s).
The below example is looking to identify and keep all data within the DataTablewhose ID is less than 3. Even though the Excel document where the data was takenfrom was a whole integer, UiPath interprets all numeric values read from anExcel document as a Double. Therefore, the Value field should reflect this.Instead of Column ID being less than or equal to "3" it must be set as "3.00".
The Output Columns tab allows the user to specify which of the columns toreturn, if the row data matches the conditions specified on the Filter Rows tab.In this example, all columns need to be returned, and so this tab is left as-is.
![](media/b4a916bf88bc290acaae62c6cf5d8671.png)
![](media/d0e97c967c507f4d00cc78a73d623915.png)
The user is able to add data to a DataTable object by using the Add Data RowActivity, with data being supplied as an ArrayRow or as an actual DataRow.
![](media/f651440cb9c880ac98303001e32e7ade.png)
## Tutorial
## Exercises
