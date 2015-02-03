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
