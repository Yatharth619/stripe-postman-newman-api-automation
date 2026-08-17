# Stripe Postman Newman API Automation

API automation project built using **Postman, JavaScript, Newman, and GitHub Actions** to test the Stripe Sandbox API.

## Tech Stack

- Postman
- JavaScript
- Newman
- Stripe API
- Git & GitHub
- GitHub Actions

## What I Automated

- Customer CRUD operations
- Product creation and retrieval
- Price creation
- PaymentIntent creation and confirmation
- Positive and negative API scenarios
- Response validation and data type checks
- Dynamic ID handling between requests
- Status code and response validation

## CI Automation

The Postman collection is executed automatically using **Newman through GitHub Actions**.

```text
Git Push
   ↓
GitHub Actions
   ↓
Newman
   ↓
Stripe Sandbox API
   ↓
Assertions
   ↓
HTML Test Report
```

The Stripe secret key is stored securely using **GitHub Actions Secrets** and injected at runtime.

## Postman Collection

The collection contains automated API tests for customers, products, prices, and payments.

**Postman Collection Screenshot**

<img width="487" height="573" alt="image" src="https://github.com/user-attachments/assets/ce0993a6-b604-41f0-ad9c-b9ba73c962a5" />


## Test Results

**12 requests | 38 assertions | 0 failures**

**Newman HTML Report Screenshot**

<img width="931" height="887" alt="image" src="https://github.com/user-attachments/assets/fdf6924d-5d1a-4bf9-8267-3113c2db87c1" />


## GitHub Actions

The API test suite runs automatically through GitHub Actions whenever changes are pushed to the repository.

**GitHub Actions Screenshot**

<img width="1578" height="786" alt="image" src="https://github.com/user-attachments/assets/4ca1964b-0530-44fd-af54-b28adac4c371" />


## Reporting

Newman generates an HTML test report after execution. The report is uploaded as a **GitHub Actions artifact**, allowing the test results to be accessed from each workflow run.

## Security

The Stripe secret key is not stored in the repository.

The key is stored securely using **GitHub Actions Secrets** and injected into Newman at runtime.

## Project Structure

```text
.github/workflows/   → GitHub Actions workflow
postman/             → Postman collection & environment
reports/             → Generated Newman reports
README.md            → Project documentation
```
