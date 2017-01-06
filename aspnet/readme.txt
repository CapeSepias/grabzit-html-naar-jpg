GrabzIt 2.3
===========

This library allows you to programmatically convert web pages into images, PDF's, CSV's and spreadsheets. Additionally GrabzIt allows you to convert online videos into animated GIF's.

It is usually best to place these files in their own directory.

To run the samples

Open the GrabzIt solution file.

Screenshots in Web Applications
===============================

The solution contains a project called Sample, which is a example web application.

+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
+ As this example uses a callback handler it must be deployed to a publicly accessible web server.+
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

To configure this do the following:

Then open web.config and change the application key and application secret to match your settings the first two parameters can be got from https://grabz.it/api

  <appSettings>
    <add key="ApplicationKey" value="APPLICATION KEY"/>
    <add key="ApplicationSecret" value="APPLICATION SECRET"/>
  </appSettings>

Next add the GrabzIt http handler to the web.config with the location it is currently stored at.

      <httpHandlers>
        <add verb="*" path="GrabzIt.ashx" type="GrabzIt.Handler, GrabzIt" />
      </httpHandlers>

Ensure your application has read and write access to the "screenshots" directory.

Finally run the Default.aspx to start taking screenshots.

Screenshots in Windows Applications
===================================

The solution also contains a project called SampleConsole, which is a example windows console application. To configure this do the following:

Then open App.config and change the application key and application secret to match your settings the first two parameters can be got from https://grabz.it/api

  <appSettings>
    <add key="ApplicationKey" value="APPLICATION KEY"/>
    <add key="ApplicationSecret" value="APPLICATION SECRET"/>
  </appSettings>
  
Finally run the console application to create screenshots in windows.





More documentation can be found at: https://grabz.it/api/aspnet