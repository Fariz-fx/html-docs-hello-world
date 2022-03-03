---
topic: HTML Hello World
languages:
  - HTML
products:
  - Azure App Service
  - Azure Web Apps
---

# HTML Hello World

This sample demonstrates a tiny Hello World HTML app for [App Service](https://docs.microsoft.com/azure/app-service).

# Contributing

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.


# Bash command

Folder creation and making use of git:
mkdir htmlapp
cd htmlapp
git clone https://github.com/Fariz-fx/html-docs-hello-world.git

cd html-docs-hello-world
az webapp up --location <myLocation> --name <myAppName> --html
This command may take a few minutes to run. While running, it displays information similar to the example below. Make a note of the resourceGroup value. You need it for the Clean up resources section later.

{
"app_url": "https://<myAppName>.azurewebsites.net",
"location": "westeurope",
"name": "<app_name>",
"os": "Windows",
"resourcegroup": "<resource_group_name>",
"serverfarm": "appsvc_asp_Windows_westeurope",
"sku": "FREE",
"src_path": "/home/<username>/demoHTML/html-docs-hello-world ",
< JSON data removed for brevity. >
}

Open a browser and navigate to the app URL (http://<myAppName>.azurewebsites.net) and verify the app is running - take note of the title at the top of the page. Leave the browser open on the app for the next section.

Update and redeploy the app
In the Cloud Shell, type code index.html to open the editor. In the <h1> heading tag, change Azure App Service - Sample Static HTML Site to Azure App Service Updated - or to anything else that you'd like.
Use the commands ctrl-s to save and ctrl-q to exit.
Redeploy the app with the same az webapp up command. Be sure to use the same values for <myLocation> and <myAppName> as you used earlier.
az webapp up --location <myLocation> --name <myAppName> --html
Tip: You can use the up arrow on your keyboard to scroll through previous commands.
Once deployment is completed switch back to the browser from step 2 in the “Create the web app” section above and refresh the page.
