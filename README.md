import java.util.ArrayList;
import java.util.List;

public class AirportManager {
    private List<Flight> flights;
    private List<Passenger> passengers;

    // Constructor
    public AirportManager() {
        flights = new ArrayList<>();
        passengers = new ArrayList<>();
    }

    // Method to add a new flight
    public void addFlight(Flight flight) {
        flights.add(flight);
    }

    // Method to add a new passenger to a flight
    public void addPassenger(Passenger passenger) {
        passengers.add(passenger);
    }

    // Method to display all flights
    public void displayFlights() {
        for (Flight flight : flights) {
            System.out.println("Flight Number: " + flight.getFlightNumber());
            System.out.println("From: " + flight.getOrigin() + " To: " + flight.getDestination());
            System.out.println("Departure Time: " + flight.getDepartureTime());
            System.out.println("-------------------------");
        }
    }

    // Method to display passengers of a specific flight
    public void displayPassengers(String flightNumber) {
        for (Passenger passenger : passengers) {
            if (passenger.getFlight().getFlightNumber().equals(flightNumber)) {
                System.out.println("Passenger Name: " + passenger.getName());
                System.out.println("Seat Number: " + passenger.getSeatNumber());
                System.out.println("-------------------------");
            }
        }
    }

    // Other methods as needed
}
