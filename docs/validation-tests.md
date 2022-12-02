---
id: validation-tests
title: Validation Tests
sidebar_label: Validation Tests
---

## Build

The build for the validation tests will be whole system, including all 4 modules.

## Purpose

 The purpose of this build is to test the system against user requirements. We will test the system as a whole to validate that it meets those requirements. Besides those, we will test the response time and precision of the system, as they are important to user experience. A traceability matrix will be provided at the end, mapping each test case to requirements.

## Tests

__Test 1:__ Test if use can update different system setting via user interface

- Turn on and off monitoring under different settings, and check the system’s status
- Change monitoring settings when system is on, and check the system’s action
- Turn on and off alert, trigger an event, and check the system’s action
- Turn on monitoring for a period of time, view the detailed report, and check the information provided
- Use the system to monitor a user for a few periods of time, view personalized analysis of factors, and check for correctness and accuracy

__Test 2:__ Test if the system is able to continuously monitor and process data

- Turn on the system for a period of time, and check details about environment conditions in the report for accuracy
- Turn on the system for a period of time, and check details about user’s health condition and sleep data in the report for accuracy
- Turn on the system, ask the monitored user to get out of the range of the sensor for a period of time, and check the reaction of the system

__Test 3:__ Test if the system is able to notify user to predefined conditions in real-time

- Turn on the system, ask the monitored user to simulate a sleep apnea (repeatedly stops and starts breathing), and check system’s reaction
- Turn on the system, create one of the predefined conditions, and check the system’s reaction (repeat this procedure for all predefined conditions)
- Turn on the system, set one or more user defined conditions, create one of these conditions in reality, and check the system’s reaction (repeat this procedure for all user defined conditions)
- Turn on the system, create a condition for which adjusting the height of Sleep Bed can be a solution, and check the system’s and Sleep Bed’s reaction (may repeat this procedure with different problems with different severity to test if the system can take continuous actions to fix the problem)
- Turn on the system, create a condition for which adjusting Nest Thermostat can be a solution, and check the system’s and Nest Thermostat’s reaction (may repeat this procedure with different problems with different severity to test if the system can take continuous actions to fix the problem)

__Test 4:__ Test for various nonfunctional requirements

- Use the system to monitor a user for a few periods of time, then try to access the user’s health data with different identities, including logged in as the user himself/herself, logged in as someone else, or guest (no account), and check if the system disclose the information
- Do all the basic operations which user will do frequently, count the number of interactions needed to complete an operation or number of pages needed to be shown before a user gets to the desired information (may give the statistical data to potential users or let the potential users try the system and give feedback)
- Give the system to different groups of potential users, and gather their feedback about easiness of using
- Let a user open a new account or use the system as a guest, use the system for a few times, and check if the system generates customized data
- Check if the system uses a standard interface for all sensors

__Test 5:__ Test for response time and precision of the system

- Do basic operations, such as turning on and off monitor or changing sensor settings, on the system for a large amount of time, record the response time of each operation, analyze the number recorded, and verify if it is satisfactory
- Turn on the system and create a condition that needs the system’s reaction, such as adjusting Sleep Bed or pushing alerts, for a large amount of time, record the response time of each operation, analyze the number recorded, and verify if it is satisfactory
- Create a long list with possible conditions and optimal solutions, create these conditions in reality, record the system’s reaction and compare with the optimal solutions, check if the precision is satisfactory
- Create different user accounts with different data, compare the customized recommendations with precalculated data to verify the precision of the system

## Traceability Matrix

| Test Number | Requirement ID |
|-------------|----------------|
| 1 | 1 (1.1-1.5) |
| 2 | 2 (2.1-2.3) |
| 3 | 3 (3.1-3.4) |
| 4 | 5 (5.1-5.5) |
| 5 | N/A (response time and precision) |
