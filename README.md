![WP-CLI - How to manage WordPress from the command-line](https://i.ibb.co/tZY34qK/wp-cli-github.pngg)

## Workshop "WP-CLI - How to manage WordPress from the command-line" 

@ [WordCamp Europe 2021](https://europe.wordcamp.org/2021/session/wp-cli-how-to-manage-wordpress-from-the-command-line/)

WP-CLI is the official command-line interface for WordPress. It provides a collection of commands that can be used to perform various WordPress actions such as plugin & theme installations, core updates, configurations or backups without using a browser.

In this workshop, I will teach you the basics of WP-CLI and present useful commands to learn more about this powerful WordPress management and development tool. This workshop is aimed at beginner & advanced WordPress users who are not familiar with the command line yet and are looking for an easy way to get started.

---
#### Slides
You can find the slides of this workshop on [https://speakerdeck.com/](https://speakerdeck.com/marceltannich/wp-cli-how-to-manage-wordpress-from-the-command-line)

#### WP-CLI Handbook
- https://make.wordpress.org/cli/handbook/
- https://wp-cli.org/de/
#### How to install WP-CLI
- Windows: https://www.youtube.com/watch?v=sd6MWc29G84
- Mac: https://wpbeaches.com/installing-wordpress-wp-cli-macos/
- Linux: https://www.linode.com/docs/websites/cms/install-wordpress-using-wp-cli-on-ubuntu-18-04/

#### Want to try WP-CLI locally in an easy way?
- Download https://localwp.com/
- Create a new site
- Right click on the site name
- Click on "Open Site Shell" 

![](https://i.ibb.co/YbPLj80/local.png)

---
#### Global parameters
- --prompt
- --quite
- --path
- --dry_run
---

#### Help
`$ wp help`

Opens the general help

`$ wp help plugin`

Opens the help for the respective command (e.g. plugin)

---
#### Core
`$ wp core download`

Downloads the WordPress core

`$ wp core version`

Shows the current WordPress version

`$ wp core update`

Updates the WordPress core to a newer version

`$ wp core install`

Starts the standard WordPress installation process

`$ wp core install --url=mysite.server.com --title=title --admin_user=you --admin_password=Password1 --admin_email=your@email.address`

Starts the standard WordPress installation process with each parameter

`$ wp core install --prompt`

The identical command without parameters; prompts the user to enter values for all command arguments

---
#### Set WordPress options
`$ wp option update blogname "My awesome website"`

Updates your blog title

`$ wp option update blogdescription "This is the website from Marcel"`

Updates your blog description

---
#### Themes
`$ wp theme install astra --activate`

Installs & activates the Astra Theme

`$ wp theme activate astra`

If Astra Theme is already installed you can activate it using the “activate” sub command

`$ wp theme update astra`

Updates a theme

`$ wp theme update --all`

Updates all installed themes

---
#### Plugins
`$ wp plugin install wordpress-seo --activate`

Installs Yoast SEO and activates the plugin.

`$ wp plugin list`

Shows all installed plugins

`$ wp plugin install duplicate-post woocommerce elementor contact-form-7 --activate`

Installs several plugins in bulk and activates them

`$ wp plugin update wordpress-seo`

Updates Yoast SEO

`$ wp plugin update --all`

Updates all plugins

---
#### Menus
`$ wp menu create “Top-Menu”`

Creates a menu with the name “Top Menu”

`$ wp menu location list`

Shows all menus

---
#### Maintenance mode
`$ wp maintenance-mode activate`

Updates Activates the WordPress maintenance mode

`$ wp maintenance-mode status`

Shows the current status

`$ wp maintenance-mode deactivate`

Deactivates the maintenance mode

---
#### Search & Replace
`$ wp search-replace "Jack" "Paco" --dry-run`

Searches all rows for a string and replaces it - Global Parameter --dry-run will show us first the output before making changes in our tables

`$ wp search-replace "Jack" "Paco"`

Searches all rows for a string and replaces it

---
#### Cache
`$ wp cache flush`

Clears the WordPress object cache

---
#### Media 
`$ wp media regenerate`

Regenerates thumbnails 

`$ seq 500 1000 | xargs wp media regenerate`

Regenerates thumbnails from IDs 500 - 1000

---
#### User Management
`$ wp user create`

Creates a new WordPress user and shows all available parameters

`$ wp user create --prompt`

Tip: Use the global parameter --prompt to not have to remember the specific parameters

`$ wp user add-role 2 administrator`

Assigns admin rights to the user with ID “2”

`$ wp user get 2`

Returns details about the user with ID “2”

`$ wp user delete 2 --reassign=1`

Deletes the user with ID “2” and reassign all posts to user with ID “1”

---
#### Posts
`$ wp post generate`

Generates 100 dummy posts

`$ wp post generate --count=10 --post_date=2021_06_15`

Generates 10 Posts with date 2021-06-15

`$ curl -N http://loripsum.net/api/5 | wp post generate --post_content --count=10`

Generates 10 posts with 5 paragraphs of Lorem Ipsum text

---
#### Database
`$ wp db export`

Exports the database as .sql file

`$ wp db import database.sql`

Imports the database

`$ wp help db`

Shows the help for "db" command

---
#### Languages 
`$ wp language core list`

Shows all available languages

`$ wp language core install es_ES --activate`

Installs Spanish language file and activates the language

---
#### Scaffold
`$ wp scaffold _s my-theme --theme_name="Test" --author="Marcel"`

Creates a Custom Theme based on Underscores (_s)

`$ wp scaffold plugin my-plugin`

Creates a plugin boilerplate     

`$ wp scaffold block team --title="Team" --theme=astra`

Creates a new "Team" block for the "Astra" theme

---
### Let's connect!

[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/marceltannich/)](https://www.linkedin.com/in/marceltannich/)  [![Twitter Badge](https://img.shields.io/badge/-Twitter-1ca0f1?style=flat-square&labelColor=1ca0f1&logo=twitter&logoColor=white&link=https://twitter.com/MarcelTannich)](https://twitter.com/MarcelTannich) 

**[marceltannich.com](https://www.marceltannich.com/)**
