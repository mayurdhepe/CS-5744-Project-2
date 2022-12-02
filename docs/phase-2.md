---
id: phase-2
title: User Interface Data View/Manipulation Phase
sidebar_label: User Interface Data View/Manipulation Phase
---

## Build

The build for this phase consists of three of the four modules: <abbr title="Persistence Module">DE-2</abbr>
, <abbr title="Sleep Intelligence Module">DE-3</abbr>, <abbr title="User Interface Module">DE-4</abbr>.

## Purpose

The purpose of this phase is to test the behavior of the user interface as data is updated in real time and analysis of the persisted data is performed. This phase will ensure that each of the three modules receives proper notification from the others as data is created or modified. Requirements 1.1 - 1.5, and 3.1 - 3.2 will be covered in this phase.

## Test Cases

| Test | Goal | Procedure |
|------|------|-----------|
| 2.1 | User receives audible alert. | UI subscribes to alerts. Feed persistent module data that will result in alert. Ensure analysis module generates an alert. The UI should receive the alert and respond appropriately. |
| 2.2 | User does not receive alert. | UI unsubscribes from alerts. Feed persistent module data that will result in alert. Ensure analysis module generates an alert. The UI should not receive the alert. |
| 2.3 | User can view detailed report. | Feed persistent module sleep sensor data. Analysis is performed and a report is generated. The report is loaded in the UI.
| 2.4 | User can toggle monitoring | Monitoring is toggled on/off in the UI and the persistent store is updated accordingly. Feed sensor data and ensure it is only stored when monitoring is on. |
| 2.5 | User can customize sensor thresholds. | In UI set custom thresholds for various sensors. Feed data to persistent module. Analysis should run and send alerts to UI. |
| 2.6 | User can adjust sleep devices. | In UI make adjustments to sleep devices (smart beds, thermostats, etc). Observe persistent store is updated and triggers occur. |

## Additional Software

Automating this phase of the integration tests requires addressing two items. The first is in regards to the data persistence module. As tests are created there will be lots of boilerplate code created to send data to the persistence module. It may prove useful to create a tool or library that can push data in an efficient manner. The second, automating the testing of the user interface module. This is no easy task, but luckily there are third-party tools that may assist with this, for example [Appium](https://appium.io/).
