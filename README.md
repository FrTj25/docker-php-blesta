# docker-php-blesta

A Docker for [Blesta](https://www.blesta.com).

# IMPORTANT NOTE - Image not Tested - NO WARRANTY
* Original from https://github.com/eric-hansen/docker-php-blesta
* Forked and changed for own use.
* Namely made changes: Updated downloaded Blesta.ZIP to 4.4.0, image changed to php:7.2-apache, use PHP 7 AddOns (and remove mcrypt) and newer mailparse. Configure PHP7.2 with gmp instead of install via php7.0-gmp

## Blesta 4.4.0 doesn't support PHP 7.2
Blesta doesn't run at this Dockerfile, because the used iconCube Version to encode doesn't support to decode at PHP 7.2. The following error is thrown when Enter the WebPage:
**Fatal error: The file /var/www/html/app/app_model.php was encoded by the ionCube Encoder for PHP 5.4 and cannot run under PHP 7.1 or later. Please ask the provider of the script to provide a version encoded with the ionCube Encoder for PHP 7.1. in Unknown on line 0**

## How To Use

* Install [Docker](https://www.docker.com) for your system
* Run `docker build .` inside of this directory
* Run `docker container start <container ID/hash>`
* Open up `http://<container IP>/` in your browser

## Notes

* This is basically a bare-bones build file.  Some pieces might be missing for you specifically.
* While running on PHP 7 is possible with Blesta 4.0, I created this for personal use (but felt like sharing it).
* I wish I could use the Alpine build, but there's known issues with ionCube Loader and Alpine's C library.
* At time of creating this, the install page shows all green checks for requirements.
* Since this is on [Docker Hub](https://hub.docker.com/r/velaware/docker-php-blesta/) this should be usable on an EC2 AMI instance but use Elastic IP if you don't plan on keeping it running.

## TODO

- [ ] Work on PHP 7.0 support
