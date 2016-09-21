# starter-theme-openedx

![Starter theme screenshot](screenshot.png)

Starter theme for developing comprehensive theme on Open edX

## How to use

1. Change to `edxapp` user

		$ sudo -u edxapp bash

2. Create new folder on `/edx/app/edxapp/` called `themes`

		$ mkdir /edx/app/edxapp/themes

3. Move to that folder

		$ cd /edx/app/edxapp/themes

4. Clone this repo

		$ git clone https://github.com/dehamzah/starter-theme-openedx.git starter-theme

5. Make some changes in `lms.env.json` located in `/edx/app/edxapp/`. Then change some variables to this:

		ENABLE_COMPREHENSIVE_THEMING: true,
		COMPREHENSIVE_THEME_DIRS: ["/edx/app/edxapp/themes"],
		DEFAULT_SITE_THEME: "starter-theme",

6. Back to ubuntu sudo users, and restart the edxapp to load new configuration.

		$ exit
		$ sudo /edx/bin/supervisorctl restart edxapp:

7. Run the `update.sh` script. To apply the themes.

		$ cd /edx/app/edxapp/themes/starter-theme/
		$ sh update.sh



