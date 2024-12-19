# Multilayered API Security with Cognito and WAF
https://catalog.workshops.aws/well-architected-security/en-US/4-infrastructure-protection/multilayered-api-security-with-cognito-and-waf

# How to protect public API
## API Gateway
Create and Manage the API, integrate with other services to secure the API services
- Request validation against HTTP header, body, URL, query strings...
- Request Authorizers validate Token issued by Cognito pool
- Stage
- Resources
- method
- Integration


## CloudFront
- Distributed Edge location to enable cashing at edge location which reduced traffic to API gateway, which could further improve the cost
- Cloud Shield standard edition to protect Layer3 and 4 DDoS attack

## WAF
Global WAF attached to CloudFront, Regional WAF attached to API Gateway directly
- Rules to enforce the traffic coming from CloudFront by rejecting API calls without specific header attached by CloudFront
- Rule Groups, managed by AWS or 3rd party from Market place, to provide protect against cyber attack

## Cognito
- Only allowed authenticated user with issued Token to access the API gateway

## Security Manager
- store, encrypted and rotate keys.