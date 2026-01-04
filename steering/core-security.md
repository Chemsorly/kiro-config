# Security
## Purpose
Defines security practices, validation requirements, and threat mitigation strategies.

## Instructions
- Never expose credentials, tokens, or sensitive data in code or logs (ID: SECURITY_NO_CREDENTIALS)
- Validate all user inputs and file paths to prevent injection attacks (ID: SECURITY_INPUT_VALIDATION)
- Use secure session management with built-in framework features (HTTP connection ID for Blazor Server) (ID: SECURITY_SESSION_MANAGEMENT)
- Implement proper error handling that doesn't leak system information (ID: SECURITY_ERROR_HANDLING)
- Use dependency injection for testable security components without exposing internals (ID: SECURITY_TESTABLE_DESIGN)
- Sanitize file paths and prevent directory traversal attacks (ID: SECURITY_PATH_SANITIZATION)
- Implement timeout mechanisms for long-running operations to prevent resource exhaustion (ID: SECURITY_TIMEOUT_PROTECTION)

## Security Testing Requirements
- Mock external dependencies in tests to avoid exposing real credentials (ID: SECURITY_MOCK_DEPENDENCIES)
- Test error handling paths without exposing sensitive information (ID: SECURITY_TEST_ERROR_PATHS)
- Validate input sanitization with malicious input test cases (ID: SECURITY_TEST_INPUT_VALIDATION)
- Test session management edge cases and timeout scenarios (ID: SECURITY_TEST_SESSION_EDGE_CASES)

## Dependency Security
- Use package evaluation criteria that includes security vulnerability assessment (-30% confidence) (ID: SECURITY_PACKAGE_EVALUATION)
- Avoid packages with unresolved security issues or poor maintenance records (ID: SECURITY_AVOID_VULNERABLE_PACKAGES)

## Priority
Critical

## Error Handling
- Log security events without exposing sensitive details
- Implement graceful degradation for security failures
- Document security decisions and trade-offs in lessons-learned