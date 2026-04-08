# Integration Guide for Kenya Payment Gateway

## Table of Contents
1. Introduction  
2. Prerequisites  
3. Step 1: Setup Environment  
4. Step 2: API Key Configuration  
5. Step 3: Implementing API Calls  
6. Step 4: Testing Integration  
7. Troubleshooting  
8. Additional Resources  

---

## 1. Introduction
This guide provides a step-by-step approach for developers to integrate with the Kenya Payment Gateway.

## 2. Prerequisites
- Basic knowledge of RESTful APIs  
- Programming language of choice (e.g. Python, Java, PHP, etc.)  
- A valid API key from Kenya Payment Gateway.

## 3. Step 1: Setup Environment
- Set up your development environment using your chosen programming language.  
- Ensure you have any necessary libraries or dependencies installed.

## 4. Step 2: API Key Configuration
- Navigate to the Kenya Payment Gateway dashboard to obtain your API key.  
- Store the API key securely in your application's environment variables.

## 5. Step 3: Implementing API Calls
- Use the following endpoints to interact with the payment gateway:
  - **Initiate Payment:** `POST /payments/initiate`
  - **Check Payment Status:** `GET /payments/status`

- Example implementation:
```python
import requests

API_KEY = 'your_api_key'
BASE_URL = 'https://api.kenyapayments.com'

# Function to initiate payment
def initiate_payment(amount):
    response = requests.post(f'{BASE_URL}/payments/initiate', json={'amount': amount}, headers={'Authorization': f'Bearer {API_KEY}'})
    return response.json()
```

## 6. Step 4: Testing Integration
- Utilize the sandbox environment to test your integration thoroughly before going live.

## 7. Troubleshooting
- Common issues:
  - Invalid API key  
  - Network connectivity issues  
- Refer to the error messages returned from the API for guidance.

## 8. Additional Resources
- [API Documentation Link]  
- [Support Contact Information]  
