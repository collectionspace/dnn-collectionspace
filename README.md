# DNN-collectionspace

A DNN plugin for CollectionSpace.

.Net Framework version >=4.7.1

This plugin embeds a CollectionSpace collection browser into your DNN site. To use this plugin, you must have a CollectionSpace 6.0 (or above) installation that has been configured to index records into an Elasticsearch cluster.

## Installing the Plugin

To install the plugin, Upload The Zip file to your DNN server.

1.Download the plugin source code.

```bash
git clone https://github.com/collectionspace/dnn-collectionspace.git
```

2. You need to generate a build from the source code. Install the visual studio 2019 or any latest available.

3. On Visual studio landing screen select **open a project or a solution**

4. Navigate to your project root and select **cspace.sln** file.

5. In the project explorer expand references you will see unresolved references we need to install them.The quickest way to do this is to remove DotNetNuke.Web.MVC from the list and right click on **References** and **Manage Nuget Packages**

6. Click on browse and search for DotNetNuke.Web.Mvc and hit install. The process should take some time but should install most of the dependencies.

7. After that select release from dropdown the default value should be debug and click on Built -> Build Solution  

6. On the root of your project you should now see a Install Folder.

5. on the top toolbar select release from the dropdown and click Build ->Generate Build 

2. In the DNN Admin sidebar, click Setting, click the **Extensions** options, then click the **Install Extension** button. 

3. Select the **cspace_00.00.01_Install.zip** file located at **install** folder on root and upload it.
4. Keep on pressing yes for all of the screens that comes next.

## Configuring the Plugin

The following instructions describe how to configure the plugin using the DNN admin area.

### Adding a CollectionSpace Browser
1. After successfully installing the Module you need to go to the page where you want to browser to show.
2. Click on Extensions button located at the bottom of the page.
3. Drag the plugin to your desired location on the page.
4. Click on the pencil icon to add configuration for the Collectionspace browser.
3. You will need to add two values **Script Location** and **config** all of these values are required
4. script location: The URL to the CollectionSpace browser JavaScript application. Your CollectionSpace administrator should be able to provide the correct value for your CollectionSpace installation.
```
https://unpkg.com/cspace-public-browser@1.1.0/dist/cspacePublicBrowser.min.js
```
5. config: Configuration settings for the CollectionSpace browser application, in JavaScript object notation (not restricted to JSON).The **basename** is important. e.g if your page name is collectionspace then add the basename like given below.
```
{
      basename: '/collectionspace',
     "gatewayUrl": "https://core.dev.collectionspace.org/gateway/core"
}
```
6. Click Save and the page should reload with the browser up and running.

