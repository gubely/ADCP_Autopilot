# Getting Started

1. Mission Planner installieren: https://ardupilot.org/planner/docs/mission-planner-installation.html
2. Firmware auf Pixhawk 4 laden: https://ardupilot.org/planner/docs/common-loading-firmware-onto-pixhawk.html#common-loading-firmware-onto-pixhawk
3. Pixhawk korrekt montieren: https://ardupilot.org/rover/docs/common-mounting-the-flight-controller.html
4. Hardware korrekt anschliessen: https://docs.px4.io/master/en/power_module/holybro_pm07_pixhawk4_power_module.html
5. Korrekte Orientierung der Hardware sicherstellen (Pfeile): https://docs.px4.io/v1.9.0/en/assembly/quick_start_pixhawk4.html
6. Sicherstellen, dass das interne XJT Modul und die Empfänger die selbe Firmwareversion haben. Ansonsten flashen.
7. FrSky Fernsteuerung mit Empfänger binden: https://www.youtube.com/watch?v=caHT-QZNliI
8. Fernsteuerung kalibrieren: https://ardupilot.org/rover/docs/common-radio-control-calibration.html
9. Interner Beschleunigungssensor (auf Pixhawk 4) kalibrieren: https://ardupilot.org/rover/docs/common-accelerometer-calibration.html
10. Kompass kalibrieren: https://ardupilot.org/rover/docs/common-compass-calibration-in-mission-planner.html
11. Motor Konfiguration auf **Skid Steering** (wie R2D2) stellen:
    * `SERVO1_FUNCTION` = 73 (Throttle Left)
    * `SERVO3_FUNCTION` = 74 (Throttle Right)
	* `MOT_PWM_TYPE` = 0 (Normal)
	* `FRAME_CLASS` = 2 (Boat)
	* `FRAME_TYPE` = 0 (Undefined)
	* `BRD_SAFETYENABLE` = 0 (Disabled, kein Notaus)
	* `PILOT_STEER_TYPE` = 0 (default, noch unklar)
12. Schalter für Arming/Disarming konfigurieren: https://ardupilot.org/rover/docs/arming-your-rover.html
	* CH7 als Auxiliary Switch einrichten (Channels 1-4, 5 und 8 sind reserviert)
	* `RC7_OPTION` = 41
13. **Flugmodi** einstellen: https://ardupilot.org/rover/docs/common-rc-transmitter-flight-mode-configuration.html
14. Pre-Arm Checks konfigurieren: https://ardupilot.org/rover/docs/parameters.html#arming-check
	* `ARMING_CHECK` = 1047998 (Pre-Arm Checks der RC Channels werden so deaktiviert).
15. Unter **Radio Calibration** kontrollieren, dass alle Switches:
	* mehr als 1800 anzeigen, wenn HIGH geschaltet.
	* weniger als 1200 anzeigen, wenn LOW geschaltet.
16. Tote Zone der Motoren einstellen: https://ardupilot.org/rover/docs/rover-motor-and-servo-configuration.html#minimum-throttle
17. Telemetry Radio v3 aufsetzen:
	* Telemetry Radio v3 mit USB verbinden.
	* Falls Modul nicht als COMport im Gerätemanager erscheint: Treiber `CDM212364_Setup.exe` installieren (Ordner `...\src\telemetry_radio_v3_win_driver`)
	* Mit Modul verbinden: https://ardupilot.org/copter/docs/common-configuring-a-telemetry-radio-using-mission-planner.html
	* Autopilot mit Telemetrie Modul verbinden: https://ardupilot.org/planner/docs/common-connect-mission-planner-autopilot.html

# Hardware Setup
* Airframe definieren: https://docs.px4.io/v1.9.0/en/airframes/airframe_reference.html
* Verbindung zwischen PM und Flightcontroller: https://docs.px4.io/v1.9.0/en/assembly/quick_start_pixhawk4.html

# Weitere Schritte
* https://ardupilot.org/rover/docs/rover-tuning-throttle-and-speed.html
* Tune `CRUISE_SPEED`: https://ardupilot.org/rover/docs/rover-tuning-process.html#tune-the-speed-and-throttle-controller
* Power Setup kalibrieren: https://docs.qgroundcontrol.com/master/en/SetupView/Power.html

# Missions
* Auto Mode einstellen: https://ardupilot.org/rover/docs/auto-mode.html
* https://ardupilot.org/rover/docs/learning-a-mission.html
# Konfiguration

## v01
* Erste funktionierende Konfiguration.
* Tote Zone der Motoren eingestellt (`MOT_MIN_THR` = 12).

## v02
* Flugmodi von CH8 neu eingestellt, dass `Flight Mode 6` = Acro ist.
* `CH9` als AUX function für `LearnCruise` eingestellt.
* RC Calibration nochmals ausgeführt.


# Links
* Glossar: https://ardupilot.org/planner/docs/common-glossary.html#common-glossary
* Autopilot In-/Outputs: https://ardupilot.org/rover/docs/common-flight-controller-io.html#common-flight-controller-io
* FrSky Fernsteuerungen: https://ardupilot.org/rover/docs/common-frsky-rc.html
* Radio Control Systems: https://ardupilot.org/rover/docs/common-rc-systems.html#common-rc-systems
* Kompatible QX7 Empfänger: https://www.horusrc.com/en/blog/frsky-qx7-compatible-receivers/
* How to Bind QX7 with FrSky Receiver: https://www.youtube.com/watch?v=caHT-QZNliI
* Loiter Mode für Boote: https://ardupilot.org/rover/docs/loiter-mode.html
* Boogieboard Referenz: https://ardupilot.org/rover/docs/reference-frames-boogieboard-boat.html
* Skid Steering Setup (PILOT_STEER_TYPE = 3): https://discuss.ardupilot.org/t/boat-skid-steer-setup-issue/49350
* Control modes anpassen: https://ardupilot.org/rover/docs/rover-control-modes.html
* Firmware von Empfänger flashen? https://www.youtube.com/watch?v=eYVk2lWPJxU
* Motorenregler Quark Plasma Monster Hybrid: http://www.offroad-cult.org/Board/quark-plasma-monster-hybrid-180a-regler-details-t20608.html
* Zugelassene Sendeleistung für Telemetrie: https://www.ofcomnet.ch/api/rir/1021

# Bestellen bzw. Organisieren
* SD Karte!
* Natoknochen
* 10 Pin Kabel
* Antenne für QX7
* USB Mini Kabel