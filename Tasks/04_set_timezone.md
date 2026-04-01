# Timezone set

This step is important for correctly track logs, scheduled tasks and easier debugging. 

## Objectives

Set the system timezone according to current location - GMT +3 & verify the results 

## Steps and Commands

1. timedatectl - used this command to see the current date and time

![date](https://github.com/user-attachments/assets/0aadb248-edc2-45b4-88a1-071fdd1744a5)

2. timedatectl list-timezones | grep Bucharest - used this pipe command to see if current location is availalbe

3. timedatectl set-timezone 'Europe/Bucharest' - used to set the timezone based on the system location

4. date - used to verify the current timezone

![timezoneset](https://github.com/user-attachments/assets/5a8f8224-b48a-4306-824e-10f02040f0c5)

