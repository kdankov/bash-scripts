## Scripts

### create-vhost

1. Creates a site folder
2. Setup & configuration of apache vhosts
3. Adds the vhost name to the hosts file

Used in `wp-install`

### wp-install

1. Downloads, Configures and installs latest version of WordPress
2. Installs and Activates a custom theme.

Uses both `create-vhost` and `consular-install-project`

### consular-install-project

1. Creates a new Consular project for `wp-install`

## Assumptions

* Local sites can have the same name for VHost, Site folder, theme folder, Datanase name, Database user
* Apache uses VHosts
* Apache uses single VHost file for each VHost

## Global variables needed

You need these variables in your bash environment:

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

