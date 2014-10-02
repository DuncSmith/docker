Tortuga-dock
============

A Dockerized Sabnzbd and Sickbeard Container.

Installation
------------

1. `git clone git@github.com:DuncSmith/docker.git docker`
2. `cd tortuga`
3. Update `autoProcessTV.cfg` with the username and password that you'll be using for your sickbeard instance. 
4. `make build`
5. `make run`

Sabnzbd Configuration
---------------------

Visit http://***server address***:8080 and follow the sabnzbd wizard to set up your newsfeed provider and initial settings.

Once sabnzbd has restarted, reload the site and click **config**. You can now configure Sabnzbd, don't forget to save each section of the setup process before moving to the next.

### General

* Configure a username and password for accessing. Don't forget this.
* Take note of the API key you'll need this to configure sickbeard shortly.

### Folders

* Temporary Download folder `Downloads/incomplete`
* Completed Download folder `Downloads/complete`
* Post-Processing Scripts Folder `/opt/sickbeard/autoProcessTV`

### Categories

* Add a new Category `TV` and select `sabToSickBeard.py` in the script dropdown.

Sickbeard Configuration
-----------------------

Open http://***server address***:8081. Click Config.

### General

* Untick Launch Browser, we're not running in Windows!
* Configure your Username and Password, these should be the same you provided in `autoProcessTV.cfg` above.

### Search Settings

#### NZB Search

* NZB Method `SABnzbd`
* Enter your Sabnzbd server address, user credentials and API Key as configured earlier
* SABnzbd Category `TV`
* Hit *Test SABnazbd* to ensure everything works

That's it - you should be good.

