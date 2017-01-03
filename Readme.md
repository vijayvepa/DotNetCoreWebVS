### Project Creation

From command line, this project's equivalent could have been created with 
`dotnet new -t web`

This project was created in Visual Studio-> add -> New Project-> .NET core -> Empty


### Configuration

#### Change Server Port

- In Program.cs, change the value of the following code for kestrel server

`.UseUrls("http://localhost:8081");`
- In Properties\launchSettings.json, change the following line to allow Visual Studio to launch new port:

`"launchUrl": "http://localhost:8081",`

#### Change Environment name:

- In Properties\launchSettings.json, change the following:

`    
	  "environmentVariables": {
        "ASPNETCORE_ENVIRONMENT": "Stage"
      }
`



### Sample Functionality

#### Static Files

- Make sure in Startup.cs, the following code is uncommented:

`app.UseStaticFiles();`
- go to http://localhost:8081/test.html
- Expect to see the static content in test.html

#### Directory Browsing

- In Startup.cs, make sure the following code is uncommented:
`app.UseDirectoryBrowser();`
- go to http://localhost:8081 
- Expect to see the directory listing.












