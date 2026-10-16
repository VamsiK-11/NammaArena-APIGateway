# NammaArena - API Gateway

API Gateway for the NammaArena microservices architecture, built with Spring Cloud Gateway. Handles routing, JWT authentication and CORS.

## Tech Stack
- Java 17
- Spring Boot 3.2.0
- Spring Cloud Gateway
- Spring Security
- JWT (jjwt 0.11.5)

## Port
`8080`

## Getting Started

### Prerequisites
- Java 17
- Maven 3.9+
- Eureka Server running on port 8761

### Run Locally
```bash
mvn clean package -DskipTests
java -jar target/*.jar
```

### Run with Docker
```bash
docker build -t nammaarena-api-gateway .
docker run -p 8080:8080 nammaarena-api-gateway
```

## Routes
| Route | Service | Path |
|---|---|---|
| `/auth/**` | auth-service | `/api/auth/**` |
| `/turfs/**` | turf-service | `/api/turfs/**` |
| `/bookings/**` | booking-service | `/api/bookings/**` |
| `/payments/**` | payment-service | `/api/payments/**` |

## Part of NammaArena Microservices
| Service | Repository |
|---|---|
| Eureka Server | [NammaArena-EurekaServer](https://github.com/VamsiK-11/NammaArena-EurekaServer) |
| API Gateway | [NammaArena-APIGateway](https://github.com/VamsiK-11/NammaArena-APIGateway) |
| Auth Service | [NammaArena-AuthService](https://github.com/VamsiK-11/NammaArena-AuthService) |
| Turf Service | [NammaArena-TurfService](https://github.com/VamsiK-11/NammaArena-TurfService) |
| Booking Service | [NammaArena-BookingService](https://github.com/VamsiK-11/NammaArena-BookingService) |
| Payment Service | [NammaArena-PaymentService](https://github.com/VamsiK-11/NammaArena-PaymentService) |
