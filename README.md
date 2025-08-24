Live Delivery Order Tracker Simulation  
A Python-based command-line simulation models a real-time food and package delivery system. This project shows important ideas in logistics, location tracking, and predicting delivery times in an active, multi-order setting.  

Key Features  
Real-Time Simulation: Watch multiple delivery orders move from "Pending" to "Delivered" in a live, continuously updating command-line interface.  

Geospatial Calculations: It uses the Haversine formula to calculate distances between geographical coordinates (latitude and longitude) accurately.  

Dynamic Order Management: Orders are created with random start and end locations. They are assigned to drivers and tracked individually.  

AI-Powered ETA Prediction: The project includes a simple AI component that calculates and updates the Estimated Time of Arrival (ETA) for each order based on its remaining distance and average speed.  

Clear and Detailed Status Updates: Each order's status, current location, progress percentage, and ETA display in a clean, easy-to-read format.  

How It Works  
The simulation is built around a DeliveryOrder class that manages the state of each order. Here’s a breakdown of the logic:  

Initialization:  
Multiple orders are created with random start and end coordinates within a defined radius of a central point (New Delhi).  

The total delivery distance for each order is calculated using the Haversine formula.  

Driver Assignment:  
Drivers are assigned to orders, changing their status from PENDING to PICKED_UP. This action triggers the first ETA calculation.  

Movement Simulation:  
The main simulation loop runs at a fixed interval (e.g., every 5 seconds).  

For each active order, the script simulates movement by calculating a new set of coordinates along the straight-line path from the current location to the destination.  

The distance moved in each step is based on a constant average speed.  

AI-Based ETA Prediction:  
With every location update, the AI component recalculates the remaining distance to the destination.  

It predicts the time needed to cover this distance and updates the order's ETA. While this is a simplified model, it lays the groundwork for a more advanced system that could use machine learning models trained on traffic, weather, and time-of-day data.  

Completion:  
Once an order reaches its destination, its status updates to DELIVERED, and it no longer updates in the simulation.  

How to Run  
Prerequisites: Ensure you have Python 3 installed on your system.  

Save the Code: Save the provided script as a Python file (e.g., delivery_tracker.py).  

Execute from Terminal: Open your terminal or command prompt, navigate to the directory where you saved the file, and run the following command:  

python delivery_tracker.py  

Observe the Simulation: The simulation will start running in your terminal. Status updates for all orders will print every 5 seconds.  

Stop the Simulation: Press Ctrl+C to stop the simulation at any time. A final status report of all active orders will display.
