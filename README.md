# speed-limit-fine-calculator-1q2023

You are running a transportation company, and your negligent drivers exceed the speed limit over and over again.

Every time you want to find out how much you will pay for their mistakes, you have to google the speed limits and the fines. You decided to create a console app that asks the vehicle type, the road type, and the speed of the vehicle, and calculates the ticket.

We have three types of vehicles: car, bus and truck. The speed limit values are the following (in km/h):

Vehicle Type	Urban Areas	Main Roads	Highways
Cars	        50	        90	        130
Buses	        50	        70	        100
Trucks	        50	        70	        80
When developing the app, please keep in mind the architectural principles you've acquired in the Basic Architecture section of this chapter. Your application should:

satisfy the Single Responsibility Principle,
use the Interface Segregation Principle,
use Dependency Injection,
include logging of the operations,
follow Clean Code Principles.
The interfaces have been provided in the starter code. You need to plug in the implementations and make the application work.

1. Vehicle speed limit provider
   You need to implement the interface called VehicleLimitProvider, in a class that is going to be responsible for providing the speed limit values for different vehicles on different roads.

This example includes three vehicle types with the following speed limits.

Cars are limited to 50 in urban areas, 90 on main roads, and 130 on highways.

Buses are limited to 50 in urban areas, 70 on main roads, and 100 on highways.

Trucks are limited to 50 in urban areas, 70 on main roads, and 80 on highways.

An implementation of the VehicleLimitProvider is created and placed in a package called service.

The implementation contains a method that receives a vehicle type and a road type, then returns the correct speed limit value.

2. Speed limit fine calculator
   The next step is to create the SpeedLimitFineCalculatorImpl class. That calculates the value of the fine based on the vehicle type, the road type, and the speed of the vehicle.

An implementation of the SpeedLimitFineCalculator is created and placed in a namespace called service. The implementation contains a method that receives a vehicle type, a road type and a vehicle speed, then returns the correct fine value.

3. Fine calculator UI
   We need a class that handles user interaction. Complete the FineCalculatorUI that asks for the three inputs (vehicle type, road type, vehicle speed), invokes the necessary components to calculate the value of the fine, and then displays the results. To make things simpler, you don't need to use interfaces with UI classes.

FineCalculatorUI gets the user input, delegates the fine calculation to the SpeedLimitFineCalculator, and displays results.

4. Application
   Finally, an Application class is needed with a main method, which will be the entry point of the program. The task of this class is to create the necessary components and then invoke the UI.

The main method of the Application class is implemented, it handles the instantiation of the components, and invokes the UI