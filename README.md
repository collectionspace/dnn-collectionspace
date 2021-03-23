# DNN-collectionspace

A DNN plugin for CollectionSpace.

This plugin embeds a CollectionSpace collection browser into your DNN site. To use this plugin, you must have a CollectionSpace 6.0 (or above) installation that has been configured to index records into an Elasticsearch cluster.

## Installing the Plugin

To install the plugin, Upload The Zip file to your DNN server.

1.Download the plugin source code.

```bash
git clone https://github.com/collectionspace/dnn-collectionspace.git
```

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

