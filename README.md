# Homeassistant docker-compose 

This is a simple docker-compose file to get started with home assistant.

## How to run

Prereq:

 * docker
 * docker-compose

starting the program

 1) Either clone or simply create copy file `docker-compose.yml` in an empty
    directory. The docker-compose will create sub folders after first run.
 1) Navigate terminal to the root directory with `docker-compose.yml`
 1) Run `docker-compose up` to test while sending logs to console.
    * Navigate to `http://{ hostname or IP }:8123` in the browser.
 1) CTL+C once to gracefully shutdown once you are done testing.
 1) you should see new folders such as `config/` and `data/` which will be used
    by the container every time you start it. This includes DB files.
 1) Run permantently even after reboot with `docker-compose up -d`

## Setting up home assistant

 * Typically, the first thing to do is to add any smart devices.
   * go to `configuration` > `Devices & Services`, then `Add Integration`
   * once you have an integration added, associated devices will be available
     on the `devices` tab.
 * Update homepage lovelace (AKA overview) to have any devices and features.
 * The fun part : create automations!
   * go to `configuration` > `Automations & Scenes`, then `Add Automation`
   * create a blank automation, allows you to add triggers and events.