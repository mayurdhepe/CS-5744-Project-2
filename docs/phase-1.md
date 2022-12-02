---
id: phase-1
title: Sensor Data Persistence Phase
sidebar_label: Sensor Data Persistence Phase
---

## Build

The build for this phase consists of two of the four modules: <abbr title="Sensor Data Hub Module">DE-1</abbr>, <abbr title="Persistence Module">DE-2</abbr>.

## Purpose

The purpose of this phase is to test the behavior of the database and various system sensors as the sensors capture data and the system cleans and filters it before it is stored. Testing will ensure that the sensors are properly capturing data and filtered/transformed into a standard format for easy storage and processing. Testing will also ensure that after the data is processed that is stored correctly in the local relational database and synced with cloud databases.

## Test Cases

| Test | Goal | Procedure |
|------|------|-----------|
| 1.1  | Sensor data received/captured | Add sensor(s) to system. Verify that sensors are outputting data. |
| 1.2  | Sensor data capture triggers Sensor Data Processor | Add multiple sensors to system, including Thermometer sensor, Doppler Radar sensor, Nest thermostat, Apple Watch. Observe if this triggers the Sensor Data Processor to process the data. |
| 1.3  | Data processed into standard format. | Feed the Sensor Data Processor captured data from connected devices. Validate that it is actively converting data to the standardized format. |
| 1.4  | Erroneous data removed | Feed processed data into the Sensor Data Noise Reducer. Modify the data to include erroneous or null data points. Verify that the invalid data has been removed. |
| 1.5  | Cleaned data stored in local database | Run data through Sensor Data Noise Reducer. Verify that this triggers the Persistence Module to store the data in the local relational database. |
| 1.6  | End of sleep cycle triggers cloud data upload | Add simulated sensor data to local database. Simulate the start and end of a sleep period. Verify that ending the period triggers the Persistence Module to upload local data to cloud storage. |


## Additional Software

An important component of the sensor data hub module is its ability to process data from external sensors. It may prove useful to either mock third-party sensor data or provide a tool that can generate data based on specs from multiple third-party sleep sensors.