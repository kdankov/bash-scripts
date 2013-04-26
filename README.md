# Scripts
These are some useful scripts I wrote to automate configuration work.

## Global variables

Most scripts use these variables. Variable names should be self-explanatory.

	# Custom global vars

	export APACHE_VHOSTS_ROOT_DIR='...'
	export APACHE_VHOSTS_CONF_DIR='...'

	export MYSQL_DATA_DIR='...'
	export MYSQL_HOST='...'
	export MYSQL_ROOT_USER='...'
	export MYSQL_ROOT_PASS='...'

	export DEFAULT_MYSQL_USER_PASS='...'

	export DEFAULT_WORDPRESS_USER_NAME='...'
	export DEFAULT_WORDPRESS_USER_EMAIL='...'
	export DEFAULT_WORDPRESS_USER_PASS='...'

	export DEFAULT_DRUPAL_USER_NAME='...'
	export DEFAULT_DRUPAL_USER_EMAIL='...'
	export DEFAULT_DRUPAL_USER_PASS='...'

# General scripts

## lazyvhost-create

1. Creates a site folder
2. Setup & configuration of apache vhosts
3. Adds the vhost name to the hosts file

#### Example

	lazyvhost-create portfolio

This will create folder and setup a Vhost for 'portfolio'. Look at the source for more details.

#### Assumptions

* Local sites can have the same name for VHost, Site folder, theme folder, Datanase name, Database user
* Apache uses VHosts
* Apache uses single VHost file for each VHost

## lazyconsular-installproject

1. Creates a new Consular project that is dependant in the folder structure used in `wp-install`

# WordPress related scripts

## lazywp-install

1. Downloads, Configures and installs latest version of WordPress
2. Installs and Activates a custom theme.

Uses both `lazyvhost-create` and `lazyconsular-installproject`

#### Example

	lazywp-install portfolio

This will create and configure a VHost for 'portfolio' and then proceed to install and configure a WordPress there.

#### Assumptions

* Local sites can have the same name for VHost, Site folder, theme folder, Datanase name, Database user

## lazywp-dbexport

1. Goes to the project folder and creates a DB backup

Requires wp-cli

#### Example

	lazywp-dbexport portfolio

# Drupal related scripts

## lazydrupal-install

1. Installs & Configures a local Drupal site

#### Example

	lazydrupal-install portfolio

