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



sequenceDiagram
    participant User
    participant System
    participant Hotel
    participant Flight
    participant Payment

    User->>System: Login(username, password)
    System-->>User: Authentication successful
    User->>System: Search hotels(location, date)
    System->>Hotel: Find available hotels(location, date)
    Hotel-->>System: List of available hotels
    System-->>User: Display available hotels
    User->>System: Select a hotel
    User->>System: Search flights(location, date)
    System->>Flight: Find available flights(location, date)
    Flight-->>System: List of available flights
    System-->>User: Display available flights
    User->>System: Select a flight
    User->>System: Make a booking(hotel, flight)
    System->>Payment: Initiate payment(amount)
    Payment-->>User: Payment portal
    User->>Payment: Make payment
    Payment-->>System: Payment confirmation
    System-->>User: Booking confirmation

