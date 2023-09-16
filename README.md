# test

```mermaid

classDiagram
    class User {
        +String username
        +String password
        +String email
        +String firstName
        +String lastName
        +createAccount()
        +login()
        +logout()
    }

    class Booking {
        +Date startDate
        +Date endDate
        +String destination
        +String status
        +makeBooking()
        +cancelBooking()
    }

    class Payment {
        +Double amount
        +String paymentMethod
        +Date paymentDate
        +makePayment()
        +refund()
    }

    class Hotel {
        +String name
        +String location
        +Int numberOfRooms
        +findAvailableRooms()
        +bookRoom()
    }

    class Flight {
        +String flightNumber
        +String airline
        +String departureAirport
        +String arrivalAirport
        +Date departureTime
        +Date arrivalTime
        +findFlights()
        +bookFlight()
    }

    User "1" -- "0..*" Booking : makes >
    Booking "1" -- "1" Payment : includes >
    Booking "0..*" -- "1..*" Hotel : includes >
    Booking "0..*" -- "1..*" Flight : includes >
