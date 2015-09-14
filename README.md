# TS2 - Train Signalling Simulation

## Overview
"Train Signalling Simulation" (TS2) is a railways simulation game where you have to dispatch trains across an area and keep them on schedule. 

## Links
* [TS2 Homepage](http://ts2.github.io)
* [TS2 Code at github](http://github.com/ts2/ts2/)

## Status
Circa late 2016, this project is switching to python3 and PyQt5
TS2 Train Signalling Simulation is beta software, meaning it is playable, but lacks many features that one would expect from a simulation.
TS2 is provided with two simulations:
* A demo simulation called "drain"
* A full-featured simulation called "liverpool-st"

New simulations can be created with the editor provided with ts2.

## Installation
* Released versions:
    - Windows 64 bits: use provided installer and run ts2.exe.
    - Other platforms: see source installation.
* Source installation:
    - Download and install Python v3 or above at [www.python.org](http://www.python.org).
    - Download and install PyQt v5.o or above at [http://www.riverbankcomputing.co.uk](http://www.riverbankcomputing.co.uk).
    - Grab the sources from GitHub development page.
    - Run `ts2.py`

## Playing (QuickStart)
* Load a simulation from the _simulation_ directory (or the _data_ directory if you have installed from sources).
    If you want to load a simulation from a previous version of TS2, you will need to open it with the editor
    first and save it before loading it again in the main window.
* Route setting:
    - To turn a signal from red to green, you need to set a route from this signal to the next one.
    - To set a route left click on the signal and then to the next one. If you can create a route
        between these signals, the track between both signals is highlighted in white, the points are
        turned automatically for this route and the first signal color turn to yellow (or green if
        the second signal is already yellow or green).
    - To cancel a route, right-click on its first signal.
    - Routes are automatically cancelled by the first train passing through. However, you can set a
        persistent route by holding the shift key before clicking on the second signal. Persistent
        routes have a little white square next to their first signal.
    - Forcing route setting: It is possible to force a route setting by pressing _ctrl_ and _alt_ while
        clicking on the second signal. Beware as this will not check other conflicting routes and may result
        in train crashes or other unknown behaviour.
* Train information:
    - Click on a train code on the scene or on the train list to see its information on the
        "Train Information" window. The "Service information" window will also update.
* Station information:
    - Click on a platform on the scene to display the station timetable in the "Station information"
        window.
* Interact with trains:
    - Right click on a train code on the scene or on the "Train information" or on the "Train List"
    window to display the train menu. This menu enables you to:
        + Assign a new service to this train. Select the service in the popup window and click "Ok".
        + Reset the service. i.e. tell the train driver to stop at the first station again.
        + Reverse train. i.e. change the train direction.
    - Trains automatically change service when it is over (on drain demo BW01 becomes WB01 when reaching
    depot)
* You should see trains run, stop at red signals and at scheduled stations. They should depart at the
    departure time or after some time after the arrival time if the departure time is past.
* Scoring:
    Each time a train arrives late at a station, stops at the wrong platform or is routed to a wrong direction
    penalty points are added to the score.

