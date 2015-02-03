# DGM-Connect

# Software Requirements

* [`git`](http://git-scm.com/)
* `php`
* `apache`
* `mysql`

## Windows:

If you're not comfortable using git or navigating your folder structure with the
command line, then you may want to use
[GitHub for Windows](https://windows.github.com/).

For the PHP/Apache/MySQL requirement, the simplest solution would be to use
something like [WAMP](http://www.wampserver.com/en/). Follow the installation
instructions there.

## Mac:

If you're not comfortable using git or navigating your folder structure with the
command line, then you may want to use
[GitHub for Mac](https://mac.github.com/).

For the PHP/Apache/MySQL requirement, the simplest solution would be to use
something like [MAMP](http://www.mamp.info/en/). You only need the free version,
and the installation instructions are pretty simple.

# Installation and Setup

These instructions assume that you are using WAMP or MAMP from the requirements
above. If you are using your own method, feel free to contribute additional
instructions here.

1. Make sure you have the above software installed.

2. Download the [latest version of WordPress](https://wordpress.org/latest.zip).

3. Unzip the contents into your desired location. Be sure to move the entire
folder, and not just the contents. You don't want to miss any hidden files (such
as .htaccess).

4. Delete the `wp-contents` directory (don't worry, we'll bring it back).

5. Clone the repository as `wp-contents` in the wordpress directory.

  Command-line:
  ```bash
  cd /path/to/wordpress
  git clone git@github.com:UVU-DigitalMedia/DGM-Connect.git wp-contents
  ```

  GitHub App:

  After you've signed in, clone the repository. When it asks for the
  destination, choose the directory where your wordpress installation is, then
  change the name of it to wp-contents.

  After everything, your WordPress directory should look something like this:

  ```
  wordpress
  ├─ index.php
  ├─ license.txt
  ├─ readme.html
  ├─ wp-activate.php
  ├─ wp-admin/
  ├─ wp-blog-header.php
  ├─ wp-comments-post.php
  ├─ wp-config-sample.php
  ├─ wp-content/  # This is the repo
  │  ├─ .git/
  │  ├─ .gitignore
  │  ├─ index.php
  │  ├─ README.md # That's this file
  │  ├─ plugins/
  │  └─ themes/
  ├─ wp-cron.php
  ├─ wp-includes/
  ├─ wp-links-opml.php
  ├─ wp-load.php
  ├─ wp-login.php
  ├─ wp-mail.php
  ├─ wp-settings.php
  ├─ wp-signup.php
  ├─ wp-trackback.php
  └─ xmlrpc.php
  ```

6. Start up WAMP/MAMP and point the Apache root to your wordpress installation.

  For MAMP, click on 'Preferences', then go to the 'Web Server' tab and change
  the Document Root folder to your wordpress folder you just set up.

  For WAMP, there should be a similar process to point your Apache server to
  your wordpress installation.

  If you haven't already, click on Start Servers.

7. Next, create a database user and a database specifically for your new
  wordpress install.

  With WAMP/MAMP, it should have come with `phpmyadmin`. On your MAMP homepage,
  find the phpmyadmin link. For me it's
  [http://localhost:8888/phpMyAdmin](http://localhost:8888/phpMyAdmin).

  In phpmyadmin, click on the users tab, then click on the 'add user' link.

  For ease-of-use, create a user with the same username and password. Host is
  localhost. In the 'Database for user' section, check the checkbox next to
  'Create database with same name and grant all privileges'. Then at the bottom
  of the page, click on 'go'.

8. Now we can setup wordpress. Go to the web root in your browser. For me, it's
  [http://localhost:8888](http://localhost:8888). Go through, the installation
  steps, and when prompted, enter in your username, password, and database name
  from the previous step.

9. Once you finish with the rest of the install, you should activate
  the proper themes and plugins. Those will be listed here once this project
  gets started.

## Workflow

TODO: We need to decide on a good git workflow. The most popular model, at least
with open-source projects is distributed in nature, where everyone forks the
main repository, and then submit pull requests for changed code. This is the
safest, and probably most useful in terms of skills learned, but for those
unfamiliar with git, it can take a while to get going.
