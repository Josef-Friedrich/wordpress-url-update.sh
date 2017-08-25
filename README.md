[![Build Status](https://travis-ci.org/JosefFriedrich-shell/wordpress-url-update.sh.svg?branch=master)](https://travis-ci.org/JosefFriedrich-shell/wordpress-url-update.sh)

# wordpress-url-update.sh


## Summary / Short description

> A small shell script to update the url of wordpress sites.

## Usage

```
Usage: wordpress-url-update.sh

A small shell script to update the url of wordpress sites.

Options:
	-u MySQL user
	-p MySQL password
	-d MySQL database
	-o Old URL
	-n New URL
	-h Show usage



This script uses the mysql shell command. To use this script you must have
access to the mysql server providing the data for your wordpress site
over the shell command.

# Where is the url stored in the mysql database?

	* In the table 'wp_options' in the column 'option_value'.
	* In the table 'wp_posts' in the columns 'guid' and 'post_content'.

# Command line usage:

	wordpress-url-update.sh -u <user> -p <password> -d <database> -n <new-url>

## Example:

	wordpress-url-update.sh -u root -p 5dtaJ -d wp_db -n http://new-url.com

If you use the shell script frequently on the same site, it is recommended
to edit the script file and put there your mysql connection and url
informations:

	MYSQL_USER=""
	MYSQL_PASSWORD=""
	MYSQL_DATABASE=""
	NEW_URL=""

## Example:

	MYSQL_USER="root"
	MYSQL_PASSWORD="5dtaJ"
	MYSQL_DATABASE="wp_db"
	NEW_URL="http://new-url.com"

Then you can update your wordpress site executing this short command:

	wordpress-url-update.sh
```
## Testing

```
make test
```

