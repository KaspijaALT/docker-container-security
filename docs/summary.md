## Embedded Secrets Identified

The vulnerability scan detected embedded cryptographic keys and JWT tokens
within the container image. These findings are expected, as the application
used in this lab (OWASP Juice Shop) is intentionally vulnerable for security
training purposes.

In a production environment, embedding private keys or tokens directly in
container images would represent a critical security risk. Best practices
include using external secret management solutions such as environment
variables, cloud secret managers, or dedicated key management services (KMS).

This lab highlights the importance of image scanning and secret detection as
part of a secure container deployment pipeline.
