# Domoticz #

Script contains stand alone scripts which must be executed after booting `/etc/rc.local` or something like it.
All script have comments and the settings are stored on the top of each script.

## scripts/doorbell.py ##
Doorbell script which reads falling flank and rising flank. If margins are good (not too long / short) it will be reported to Domoticz. Requires a virtual doorsensor.

Eletronic schem to connect 8VAC to Raspberry:
[https://github.com/ericstaal/domoticz/blob/master/doorbell_scheme.png](https://github.com/ericstaal/domoticz/blob/master/doorbell_scheme.png "Scheme")

Usage:
Add script to `/etc/rc.local`

## plugins ##
All written according the new format see https://www.domoticz.com/wiki/Developing_a_Python_plugin

## plugins/wolping ##
Python plugin which combines a ping to check if a host is online and a WOL to activate it. Interval can be configured

## plugins/hosola ##
Python plugin to read out hosola / omnik solar inverters. Auto detect which phases are connected

## plugins/ledenet ##
Plugin for ledenet / Ufo RGBW led controller