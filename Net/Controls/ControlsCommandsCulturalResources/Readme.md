##Configure a command for a specific locale

###Purpose  
This sample demonstrates how resource files are used to configure an application's interface for a specific culture. This is important when developing localized applications that must use different resources at run time, depending on the user's language and location (culture).  The ResourceManager examines the application's thread user interface (UI) culture (for example, System.Threading.Thread.CurrentThread.CurrentUICulture) to determine which resource file to employ. Typically, the thread UI culture is automatically set by the operating system, but it can be temporarily overwritten to allow you to test different resource files. The application in this sample creates a tool, a command, a menu, and a pop-up menu and employs resource files to set their Icon Bitmap, ToolTip, Caption, and Message properties. The application contains three resource files—one for each of the following cultures: English (United States), French (France), and Spanish (Spain)—and are named Resources.en-US.resX, Resources.fr-FR.resX, and Resources.es-ES.resX, respectively. There is also a default resource file named Resources.resX.   


###Usage
1. Open the project file in the language of your choice, and build the solution to create an ArcGIS Engine application. This loads a command, tool, and menu using the current UI culture.   
1. Load some map data and navigate around using the tools and scroll bars in the application.  
1. Click the Culture button to use the command to identify the current UI culture this application is using.  
1. Use the Timestamp tool (with the blue clock image) to place the current time stamp on the PageLayout control. Notice that this matches the format for the selected culture.  
1. The default culture is French (France). To use a different resource file, reset the thread to a new culture by editing the Form1_Load method in either Controls/CulturalResources.cs (C#) or Controls/CulturalResources.vb (VB .NET). For example, to use the French resource file (Resources.fr-FR.resX), a French culture in the Form1_Load with System.Globalization.CultureInfo.CreateSpecificCulture has been created. Then set the current threading UI Culture to that culture. The code to set the culture to either English or Spanish is contained in that function as well and is commented out. To use a different culture, change those that are commented out and the one that is active, then recompile and rerun the sample.  
1. To create your own resource file for another culture, copy the Resource.en-US.resX file in Solution Explorer and paste it into the CultureSamples project. Rename this file the appropriate culture name. For example, change en-US to ru-RU for Russian (Russia). Change the value of any strings, but remember that the names must match those defined in the default resource file. Similarly, you can change the file name of any images, but ensure that the name is left unchanged.  







####See Also  
[IToolbarMenu2 Interface](http://desktop.arcgis.com/search/?q=IToolbarMenu2%20Interface&p=0&language=en&product=arcobjects-sdk-dotnet&version=&n=15&collection=help)  


---------------------------------

####Licensing  
| Development licensing | Deployment licensing | 
| :------------- | :------------- | 
| Engine Developer Kit | Engine |  
|  | ArcGIS for Desktop Basic |  
|  | ArcGIS for Desktop Standard |  
|  | ArcGIS for Desktop Advanced |  


