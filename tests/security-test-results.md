# Security Test Results

| Connection Path | Port | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- |
| MacBook -> Bastion | 22 | Success | Success | ✅ |
| MacBook -> App Server | 22 | Timeout | Timeout | ✅ |
| Web Tier -> App Tier | 8080 | Refused/Success | Connection Refused | ✅ |
| Web Tier -> DB Tier | 3306 | Timeout | TIMEOUT | ✅ |

### Summary
The tests verify that the Database Tier is completely isolated from the Web Tier. Traffic to the App Tier is allowed, but the Database remains unreachable from the public-facing Web Server, successfully implementing Defense-in-Depth.
