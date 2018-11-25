# docker-php-blesta

A Docker for [Blesta](https://www.blesta.com).

# IMPORTANT NOTE
Original from https://github.com/eric-hansen/docker-php-blesta
Forked and changed for own use.
Namely made changes: Updated downloaded Blesta.ZIP to 4.4.0 and change to php:7.2-apache

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
