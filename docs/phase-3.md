---
id: phase-3
title: Sleep Intelligence Analysis Phase
sidebar_label: Sleep Intelligence Analysis Phase
---

## Build

The build for this phase consists of two of the four modules: <abbr title="Persistence Module">DE-2</abbr>, <abbr title="Sleep Intelligence Module">DE-3</abbr>.

## Purpose

The purpose of this phase is to verify that the sleep intelligence module is correctly notified when new data is available and correctly pushes new data back to the persistence module upon analysis completion. The testing of this phase will not directly validate any requirements, but it does relate strongly to requirements 3.1 - 3.4 and 1.4. The data produced by the analysis is used to satisfy these requirements.

## Test Cases

| Test | Goal | Procedure |
|------|------|-----------|
| 3.1  | New data triggers analysis. | Insert new sleep sensor data into persistent module. Verify analysis is triggered and completed by the presence of additional data in storage. |
| 3.2  | Analysis triggers controlled device modification. | Insert new sleep sensor data that will force the analysis to result in recommendations for changes in controlled devices. Observe persistent module is updated accordingly. |
| 3.3  | Analysis recognizes custom alarms. | Insert a user-defined alarm and sleep sensor data into the persistent store. Verify the analysis is triggered and alerts to the possible issue. |
| 3.4  | Analysis operates in real-time. | Insert new sleep sensor data into persistent module. After analysis is triggered insert additional data. Observe the final analysis is based on recent data and not the initial data. |

## Additional Software

No additional overhead software will be required to carry out this phase of testing. If a tool is created for the [User Interface Data View/Manipulation Phase](phase-2.md) to handle inserting data in the persistence module it may also be used here to improve the efficiency of this phase.
