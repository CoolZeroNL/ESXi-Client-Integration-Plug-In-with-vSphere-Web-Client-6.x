# ESXi-Client-Integration-Plug-In-with-vSphere-Web-Client-6.x
<!-- https://www.opvizor.com/get-the-client-integration-plug-in-running-in-vsphere-web-client-6-x -->
Get the Client Integration Plug-In running in vSphere Web Client 6.x

# Install Firefox
Unfortunately, It´s not possible anymore to enable NPAPI using a Firefox version older than 52. Therefore, we need to install Firefox 52 first and uninstall any newer Version. Please be aware that Firefox autoupdates by default, so more often than not, you need to uninstall first to install an older version.

Just to make sure, you´re going to use an outdated technology. But its the only way I found that always works.

You might want to consider the Firefox Extended Support Edition that is community driven and supports NPAPI 12 month longer. https://www.mozilla.org/en-US/firefox/organizations/

Download Firefox version 52 for your OS here: https://ftp.mozilla.org/pub/firefox/releases/52.0/ and install the software. Please make sure to disable the maintenance service in the installation wizard.
<p align="center">
  <img width="75%" src="./readme.images/01.png">
</p>

Select Custom during the installation and disable the “Install Maintenance Service” Box.
<p align="center">
  <img width="75%" src="./readme.images/02.png">
</p>

## Change Update Settings
First thing to change after the first launch is the update setting.
<p align="center">
  <img width="75%" src="./readme.images/03.png">
</p>

Click the icon top right and select Options.
<p align="center">
  <img width="75%" src="./readme.images/04.png">
</p>

Disable the automatic update.

## Firefox setting to enable NPAPI
To change the NPAPI settings in Firefox and enable Flash, Silverlight plugins, just type about:config to open the advanced settings.
<p align="center">
  <img width="75%" src="./readme.images/05.png">
</p>

Accept the risk and continue to the settings page. Then right click into the list and select New-Boolean
<p align="center">
  <img width="75%" src="./readme.images/06.png">
</p>
Type in `plugin.load_flash_only` and select `false`.

<p align="center">
  <img width="75%" src="./readme.images/07.png">
</p>

<p align="center">
  <img width="75%" src="./readme.images/08.png">
</p>

Then restart Firefox.

# Install Flash
Make sure to install Flash.
<p align="center">
  <img width="75%" src="./readme.images/09.png">
</p>

# Install Client Integration Plugin
Visit your VMware vCenter Web Client and install the Client integration plugin (best is to start Firefox using an administrative account).
<p align="center">
  <img width="75%" src="./readme.images/10.png">
</p>

<p align="center">
  <img width="75%" src="./readme.images/11.png">
</p>

When everything has been installed successful, you can log into your VMware vSphere Web client and use Client Integration plugin functions like Deploy OVF.

<p align="center">
  <img width="75%" src="./readme.images/12.png">
</p>


Just make sure to allow the Plugin to do its job, by clicking allow for the https protocol access.

That’s it and you should have all up and running.
