# Ecommerce Project using Go Programming with Gin Framework
This project is an ecommerce application built using Go programming language and the Gin framework. It follows the clean code architecture, which promotes separation of concerns and maintainability.

## Project Overview
The ecommerce-gin-clean-arch project is designed to provide a performant and feature-rich ecommerce solution. It includes functionalities such as user authentication, product management, shopping cart, order processing, and payment integration.

## Used Packages
The project utilizes the following packages:
1. [GIN](github.com/gin-gonic/gin): A web framework written in Go that combines high performance with an API similar to Martini.
2. [JWT](github.com/golang-jwt/jwt): A Go implementation of JSON Web Tokens for secure authentication and authorization.
3. [GORM](https://gorm.io/index.html) with [PostgreSQL](https://gorm.io/docs/connecting_to_the_database.html#PostgreSQL): A powerful ORM library for Go that simplifies database operations.
4. [Wire](https://github.com/google/wire): A code generation tool for dependency injection, making it easier to connect components.
5. [Viper](https://github.com/spf13/viper): A configuration solution for Go applications, supporting various formats and 12-Factor app principles.
6. [swag](https://github.com/swaggo/swag) with [gin-swagger](https://github.com/swaggo/gin-swagger) and [swaggo files](github.com/swaggo/files): Converts Go annotations to Swagger Documentation 2.0 for API documentation.
7. [Google Auth][https://github.com/google/google-auth-library-go](https://pkg.go.dev/github.com/markbates/goth@v1.77.0/providers/google): A Go library for handling authentication and authorization with Google services.
8. [Twilio](https://github.com/twilio/twilio-go): A Go client library for the Twilio API, enabling communication via SMS, voice, and other channels.
9. [Razorpay](https://github.com/razorpay/razorpay-go): A Go client library for the Razorpay API, facilitating payment processing and 
management.
10. Stripe: A Go client library for the Stripe API, allowing seamless integration with Stripe's payment platform.
11. [AWS SDK](https://github.com/aws/aws-sdk-go): A comprehensive SDK for integrating Go applications with Amazon Web Services, providing functionalities for interacting with Amazon S3 and other AWS services.

Additionally, the project boasts robust CI/CD capabilities, leveraging GitHub Actions for automated build, test, and deployment processes. The source code is dockerized for seamless containerization, enhancing portability and scalability. Kubernetes (K8s) is utilized for efficient orchestration and management of containerized applications, ensuring optimal performance and scalability. This entire deployment process is demonstrated live on anyfashion.abhinand.live/swagger/index.html, providing transparency and insight into the project's deployment pipeline.

Feel free to reach out if you need further clarification or details!

# Setup Instructions
To use and test the ecommerce-gin-clean-arch project, please follow these steps:

### Prerequisites
Make sure you have the following installed on your system:
- Go (https://golang.org/doc/install)
- PostgreSQL (https://www.postgresql.org/download/)
- Twillio Account (https://www.twilio.com/en-us)
- AWS account and S3 bucket (https://aws.amazon.com/s3/)

### 1. Clone the Repository
Clone the ecommerce-gin-clean-arch repository to your local system:
```bash
git clone https://github.com/kannan112/any-fashion-gin-clean-code.git
cd any-fashion-gin-clean-code
```
### 2. Install Dependencies
Install the required dependencies using either the provided Makefile command or Go's built-in module management:
```bash
# Using Makefile
make deps
# OR using Go
go mod tidy
```
### 3. Configure Environment Variables
details provided at the end of the file
### 4. Make Swagger Files (For Swagger API Documentation)
```bash
make swag
```
# To Run The Application
```bash
make run
```
### To See The API Documentation
1. visit [swagger] ***http://localhost:8000/swagger/index.html***

# To Test The Application
### 1. Generate Mock Files
```bash
make mockgen
```
### 2. Run The Test Functions
```bash
make test
```

# Set up Environment Variables
Set up the necessary environment variables in a .env file at the project's root directory. Below are the variables required:
```.env
## Server
PORT="localhost default :8080"
### PostgreSQL database details
DB_NAME="your database name"
DB_USER="your database user name"
DB_PASSWORD="your database owner password"
DB_PORT="your database running port number"
### JWT
ADMIN_AUTH_KEY="secret code for signing admin JWT token"
USER_AUTH_KEY="secret code for signing user JWT token"
### Twilio
TWILIO_AUTHTOKEN="your Twilio authentication token"
TWILIO_ACCOUNT_SID="your Twilio account SID"
TWILIO_SERVICES_ID="your Twilio messaging service SID"
### Razorpay
RAZOR_PAY_KEY="your Razorpay API test key"
RAZOR_PAY_SECRET="your Razorpay API test secret key"
### Google Auth
GOAUTH_CLIENT_ID="your Google auth client ID"
GOAUTH_CLIENT_SECRET="your Google auth secret key"
REDIRECT_URL="your registered callback URL for Google Auth"
### Stripe
SECRET_KEY="your stripe secret key"
PUBLISHABLE_KEY="your stripe publishable key"

```
