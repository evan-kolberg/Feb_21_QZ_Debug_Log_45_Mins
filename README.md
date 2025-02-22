[SOLVED] - On the bike, the age and weight parameters were very outdated and did not match those in the QZ app

Trial 1
--------

**Describe the bug**
After a 30-minute workout, the odometer in QZ shows a much lower value than the one directly on the Schwinn 170 bike. 

QZ: 7.86 miles
Bike: 8.6 miles
--------------------
Deviation: 0.74 miles

* A ~15 second head start is expected for the bike and has no impact on odometer values
* The bike has to start a workout for Bluetooth data to be transmitted to QZ (i.e., "Quick Start" has to be pressed)
* The QZ app starts the "Time Elapsed" clock when it detects pedaling for the first time
* No stops in biking were done to cause any large deviation in both times (the bike _can_ pause if pedaling isn't done for 5-10 seconds, but QZ's time elapsed will continue. If long pauses were made, or if QZ started while the bike already had a large odometer value, that would provide an invalid case)
* Both the bike and QZ were started before pedaling, and both were stopped after pedaling ceased.


**Expected behavior**
Given that the workout wasn't too long, I expected the values to be relatively similar. I do understand that within [schwinn170bike.cpp](https://github.com/cagnulein/qdomyos-zwift/blob/master/src/devices/schwinn170bike/schwinn170bike.cpp), the displayed data within QZ are calculated based on various long decimal values.

**Screenshots**

![Image](https://github.com/user-attachments/assets/deec218d-e99d-4278-99c2-c3e66b14682c)


Graphs and Charts from the workout:

<div style="display: grid; grid-template-columns: repeat(4, 1fr); gap: 10px;">
  <img src="https://github.com/user-attachments/assets/cafec022-fa24-4427-8de9-83b7a7507f4e" width="150">
  <img src="https://github.com/user-attachments/assets/4ef2161d-c3ba-47ed-9594-b68c701ebb26" width="150">
  <img src="https://github.com/user-attachments/assets/8020d4d7-ebc1-4cf1-af07-92c3251c4074" width="150">
  <img src="https://github.com/user-attachments/assets/74a7826b-eab6-44f6-a1ac-4a603345b8bd" width="150">
  <img src="https://github.com/user-attachments/assets/a63d5ad8-6365-4c7c-873b-436764d8f301" width="150">
  <img src="https://github.com/user-attachments/assets/784b9388-fc40-474e-bc4c-6a67305c26e8" width="150">
  <img src="https://github.com/user-attachments/assets/fa1a1938-e3bc-4ab3-b754-df7205bca537" width="150">
  <img src="https://github.com/user-attachments/assets/a1b44fb3-33ef-43cd-9e8d-e5d03bed553a" width="150">
</div>



---
---

**Trial 2: 45 mins**
--------------------
Debug file: https://github.com/evan-kolberg/Feb_21_QZ_Debug_Log_45_Mins/blob/main/debug-Fri_Feb_21_18_52_30_2025.log

QZ: 11.41 miles
Bike: 12.6 miles
Deviation: 1.19 miles

Procedure: 
1. "Quick Start" was pressed on the bike
2. "Start" was pressed in QZ
3. Pedaling started and continued for 45 mins
4. The attached photo was taken

Device file: [schwinn170bike.cpp](https://github.com/cagnulein/qdomyos-zwift/blob/master/src/devices/schwinn170bike/schwinn170bike.cpp)

**Screenshots**

![Image](https://github.com/user-attachments/assets/9ce286a8-d4f8-4888-815a-46ef47021913)

Graphs and Charts from the workout:

<div style="display: grid; grid-template-columns: repeat(4, 1fr); gap: 10px;">
  <img src="https://github.com/user-attachments/assets/3252e688-7bd1-4cff-94b3-307307fdacda" width="150">
  <img src="https://github.com/user-attachments/assets/8c0db6e0-adcf-413a-846f-7374a50b1285" width="150">
  <img src="https://github.com/user-attachments/assets/babeddb3-064c-402c-be7f-52e9e218cb35" width="150">
  <img src="https://github.com/user-attachments/assets/8aca83cd-63fa-40db-a658-ec47d6005e16" width="150">
  <img src="https://github.com/user-attachments/assets/3b7637fd-a0ab-463d-ae51-61b92d7f43e7" width="150">
  <img src="https://github.com/user-attachments/assets/edccb6a8-d3ed-4ccf-89f9-78bdf59f1334" width="150">
  <img src="https://github.com/user-attachments/assets/30182411-0628-4bee-b3be-9a07c6e59666" width="150">
  <img src="https://github.com/user-attachments/assets/26034365-4fb1-4e1a-b12c-3b9ccad61656" width="150">
</div>



