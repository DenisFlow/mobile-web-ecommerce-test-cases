# Account Lockout Protection

## Test Case ID
TC-AUTH-002

## Title
Verify temporary account lock after multiple SMS requests

## Priority
Critical

## Preconditions

- User account exists
- Lockout is disabled initially

---

## Steps

### 1
Request SMS code repeatedly

### 2
Repeat 6 times within timeout window

**Expected Result**

System returns rate limit response

---

### 3
Attempt another request

**Expected Result**

User receives lockout notification

---

### 4
Wait lockout expiration

### 5
Retry request

**Expected Result**

Authentication available again