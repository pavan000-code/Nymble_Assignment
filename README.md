# Travel Agency System Documentation

## 1. Introduction

The Travel Agency System is a software system designed to assist travel agencies in managing their travel packages, itinerary, passengers, and activities. The system provides functionalities for creating and organizing travel packages, adding destinations and activities to the itinerary, signing up passengers for activities, and managing passenger details.

## 2. Classes and Functionalities

### Activity Class

- Represents an activity that passengers can sign up for at a specific destination.
- Attributes:
  - `name`: Name of the activity.
  - `description`: Description of the activity.
  - `cost`: Cost of the activity.
  - `capacity`: Maximum capacity of passengers that can sign up for the activity.
  - `destination`: Destination where the activity takes place.
  - `signedUpPassengers`: List of passengers signed up for the activity.
- Methods:
  - `signUpPassenger(Passenger passenger)`: Signs up a passenger for the activity if there is available capacity.
  - `getName()`: Gets the name of the activity.
  - `getCost()`: Gets the cost of the activity.
  - `getDestination()`: Gets the destination of the activity.

### Destination Class

- Represents a destination with a list of available activities.
- Attributes:
  - `name`: Name of the destination.
  - `activityList`: List of activities available at the destination.
- Methods:
  - `addActivity(Activity activity)`: Adds an activity to the destination's activity list.
  - `getName()`: Gets the name of the destination.

### Passenger Class

- Represents a passenger who can sign up for activities and travel packages.
- Attributes:
  - `name`: Name of the passenger.
  - `passengerNumber`: Unique identifier for the passenger.
  - `passengerType`: Type of passenger (Standard, Gold, Premium).
  - `balance`: Balance amount for the passenger (applicable to Standard and Gold passengers).
  - `signedUpActivities`: List of activities the passenger has signed up for.
- Methods:
  - `addActivity(Activity activity)`: Adds an activity to the passenger's signed-up activities list.
  - `getName()`: Gets the name of the passenger.
  - `getPassengerNumber()`: Gets the passenger number.

### TravelPackage Class

- Represents a travel package containing destinations and activities.
- Attributes:
  - `name`: Name of the travel package.
  - `passengerCapacity`: Maximum capacity of passengers for the travel package.
  - `itinerary`: List of destinations in the travel package's itinerary.
  - `passengerList`: List of passengers enrolled in the travel package.
- Methods:
  - `addDestination(Destination destination)`: Adds a destination to the travel package's itinerary.
  - `addPassenger(Passenger passenger)`: Adds a passenger to the travel package if capacity allows.

## 3. Testing

The Travel Agency System includes a unit testing class (`TravelAgencySystemTest`) using the JUnit framework. The test cases cover functionalities such as signing up passengers for activities, adding activities to destinations, adding passengers to travel packages, and capacity limits enforcement.

## 4. Conclusion

The Travel Agency System provides a comprehensive solution for travel agencies to manage their travel packages, itinerary, passengers, and activities efficiently. It offers a user-friendly interface and robust functionalities to streamline the booking process and enhance customer satisfaction.
