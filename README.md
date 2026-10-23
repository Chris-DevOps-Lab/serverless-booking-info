# Serverless Booking Info

AWS serverless booking information portfolio project.

## Architecture
Browser -> CloudFront/S3 -> API Gateway -> Lambda (Python) -> DynamoDB.
CloudWatch captures application logs. Terraform provisions infrastructure.

## Planned API
| Method | Route | Purpose |
|---|---|---|
| POST | /bookings | Create booking |
| GET | /bookings | List bookings |
| GET | /bookings/{id} | Retrieve booking |
| PUT | /bookings/{id} | Update booking |
| DELETE | /bookings/{id} | Cancel booking |

## Booking model
`bookingId`, `customerName`, `email`, `service`, `bookingDate`, `status`, `createdAt`.

## Roadmap
1. Design and repository scaffold (current)
2. Lambda CRUD implementation and unit tests
3. DynamoDB table
4. API Gateway integration
5. Frontend and CloudFront/S3 hosting
6. Terraform deployment
7. Authentication, authorization, validation and monitoring
8. GitHub Actions CI/CD and end-to-end tests

> Starter scaffold only: no AWS resources are deployed yet. Do not expose customer booking information publicly; add authorization before production use.

## GitHub setup
```bash
git init
git add .
git commit -m "Initial serverless booking architecture"
git branch -M main
git remote add origin git@github.com:YOUR_USERNAME/serverless-booking-info.git
git push -u origin main
```
Create the empty GitHub repository first. Replace YOUR_USERNAME with your username.
