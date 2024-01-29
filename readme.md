# Smark Parking lot System

## Objective
Imagine a parking lot in an urban area with **multiple floors** and **numerous parking spots**. The system should efficiently manages the parking process. The system should **automatically** assign parking spots based on **vehicle size** and **availability**, track the **time** each vehicle spends in the parking lot, and calculate **parking fees** upon exit.

## Functional Requirement
- **Parking Spot Allocation**: Automatically assign an available parking spot to a vehicle when it enters, based on the vehicle’s size (e.g., motorcycle, car, bus).
- **Check-In and Check-Out**: Record the entry and exit times of vehicles
- **Parking Fee Calculation**: Calculate fees based on the duration of stay and vehicle type.
- **Real-Time Availability Update**: Update the availability of parking spots in real-time when vehicles enter and leave.

## Low Level design

### Database Modeling
Database modeling, design and its ER diagram can be referred at [here](data-modeling.md)

### Spot Allocation Algorithm
- When a vehicle enters the system, it is assigned a parking spot based on the vehicle size and spot availability
- Assuming System has SMALL, MEDIUM, and HEAVY size vehicles. 2 Wheelers like bike or bicycle are SMALL size vehicles, wherein 3 Wheelers like car, truck, bus, etc. are MEDIUM or HEAVY size vehicles.

- Based on the vehicle size input to the entry panel, it does following steps:
  - Query for available slots, filtered by Vehicle size.
  - If slots are available, then assign the slot with a ticket to the vehicle and the slot status be updated to PARKED.
  - If no slots are available, Vehicle stays in queue and waits for a set duration for next slot availability. System keeps refreshing the availability of slots. Otherwise, vehicle gets a rejection with user message that "Parking is full".

### Parking Fee Calculation
-  When a vehicle enters the system, it
  


