# Scripts

Scripts use to automate initial setup of WordPress sites

## Assumptions

* Using Nginx for Web server
* Using Nginx for Web server
* Using Nginx for Web server

## Global variables

Most scripts use these variables. Variable names should be self-explanatory.

	export WS_VHOST_CONF_DIR='...'
	export WS_VHOST_ROOT_DIR='...'

	export MYSQL_HOST='...'
	export MYSQL_DATA_DIR='...'
	export MYSQL_ROOT_USER='...'
	export MYSQL_ROOT_PASS='...'

	export DEFAULT_MYSQL_USER_PASS='...'

	export DEFAULT_WP_USER_NAME='...'
	export DEFAULT_WP_USER_EMAIL='...'
	export DEFAULT_WP_USER_PASS='...'

# General scripts

## lazy-vhost-create

1. Creates a site folder
2. Setup & configuration of apache vhosts
3. Adds the vhost name to the hosts file

#### Example

	lazy-vhost-create portfolio

This will create folder and setup a Vhost for 'portfolio'. Look at the source for more details.

# WordPress related scripts

## lazy-wp-install

1. Downloads, Configures and installs latest version of WordPress
2. Installs and Activates a custom theme.

Uses both `lazy-vhost-create` and `lazy-consular-install-project`

#### Example

	lazy-wp-install portfolio

This will create and configure a VHost for 'portfolio' and then proceed to install and configure a WordPress there.

## lazy-wp-dbexport

1. Goes to the project folder and creates a DB backup

#### Example

	lazy-wp-dbexport portfolio
