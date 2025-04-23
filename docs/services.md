# Banking System API

Welcome to the sample documentation for a hypothetical **Banking System API**.  
This API allows third-party developers to access essential banking features such as account details, balance checks, and fund transfers.

The documentation includes authentication requirements, available endpoints, parameters, and error codes — designed to help you integrate with the API quickly and efficiently.

---

## Authentication

!!! info "API Key Required"
    All endpoints require an API key in the request header.

    ```
    Authorization: Bearer YOUR_API_KEY
    ```

---

## Base URL
https://api.bankingsystem.com/v1

---

## Endpoints

### Get Account Details

**Method**: `GET`  
**URL**: `/accounts/{account_id}`  
**Description**: Returns information about a specific bank account.

**Path Parameters**:
- `account_id`: ID of the account to retrieve

---

### Create Transaction

**Method**: `POST`  
**URL**: `/transactions`  
**Description**: Initiates a money transfer from one account to another.

#### Path Parameters

| Name         | Type     | Description               |
|--------------|----------|---------------------------|
| from_account | string   | Source account number     |
| to_account   | string   | Destination account number|
| amount       | float    | Amount to transfer        |
| currency     | string   | Currency code (e.g., USD) |
| note         | string   | Optional transfer note    |


---

### Get Account Balance

**Method**: `GET`  
**URL**: `/accounts/{account_id}/balance`  
**Description**: Retrieves the current balance of an account.

---

## Error Codes

| Code | Description             |
|------|-------------------------|
| 401  | Unauthorized            |
| 404  | Resource not found      |
| 500  | Internal server error   |
---

## Contact

For help or support, contact `support@bankingsystem.com`.

