# Parking Lot System (LLD)

## Overview
This project is a Low-Level Design (LLD) implementation of a Parking Lot Management System. The solution is built using Java and adheres to the **SOLID principles** and utilizes **design patterns** to ensure modularity and scalability. It supports multiple vehicle types, parking spot types, and payment methods.

## Features
- Multi-floor parking lot with entry and exit gates.
- Support for different parking spot types (e.g. Cars, Bikes).
- Dynamic parking spot availability display.
- Ticket generation for parked vehicles.
- Payment processing via cash, credit card, or UPI.
- Hourly Charges 

## Project Structure
The project follows a modular structure for better maintainability:

### Key Components

#### `parkinglot` package
- **ParkingLot.java**: Manages floors, entry gates, exit gates, and parking spot booking.
- **ParkingFloor.java**: Manages parking spots and updates the display board.
- **ParkingSpot.java**: Abstract representation of a parking spot (Compact, Large, etc.).
- **Ticket.java**: Represents a parking ticket issued to a vehicle.

#### `vehicle` package
- **Vehicle.java**: Abstract class for vehicles.
- **CarVehicle.java**, **BikeVehicle.java**, **OtherVehicle.java**: Specific implementations for vehicle types.

#### `payment` package
- **Payment.java**: Manages payment logic.
- **PaymentStrategy.java**: Strategy pattern for payment processing.
- **CashPayment.java**, **CreditCardPayment.java**, **UPIPayment.java**: Specific implementations for payment methods.

#### `Main.java`
- Entry point of the application. Contains the `main` method to initialize and run the parking lot system.

