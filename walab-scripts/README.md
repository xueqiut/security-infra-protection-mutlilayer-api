# walab-scripts
this script will be used to test the following Well-Architected Lab.

# MULTILAYERED API SECURITY WITH COGNITO AND WAF
https://wellarchitectedlabs.com/security/300_labs/300_multilayered_api_security_with_cognito_and_waf/

### getIDtoken.py helps you generate ID token using Amazon Cognito User Pools.

Please refer to the following format:
```sh
python getIDtoken.py <username> <user_password> <user_pool_id> <app_client_id> <app_client_secret>
```


### sendRequest.py helps send http request with ID token.

Please refer to the following format:
```sh
python sendRequest.py <URL> <ID_Token>
```

# python3 sendRequest.py 'https://d5lg0rpwrk.execute-api.us-east-1.amazonaws.com/Dev?id=1'
