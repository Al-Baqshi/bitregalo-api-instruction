# Using API Documentation

Follow the below instructions to use the API's:

## Registration API

To register a new user, send a post request to the link below with the json structure. Then you will get a success or error response like below.

```bash

# Register Url

https://albaqshi.bitregalo.com/api/register/


# JSON for registration

{
    "username": string,
    "password": string,
    "phone_number": string with '+' and country code ('if no then empty'),
    "email": string('if no then empty')
}

# Success Response

{
    "success_message": "Successfully Registered. A verification code is sent to your given Phone Number/Email. Please verify your Phone Number/Email."
}

# Error Response

{ "error_message": {another json} }

```

## Verify Registration

After completing registration user will get a email or message with a 5 digit code. You will get the code and send a post request to the following url with the json. Then you will get a valid response.

```bash

# Verify URL

https://albaqshi.bitregalo.com/api/verify-user/


# Verify JSON

{ "code": string, }

```

## Login Api

To logedin a user send the username and password as a json in a post request to the fillowing link. Then you will get a valid response with token.

```bash

# Login URL

https://albaqshi.bitregalo.com/api/login/


# JSON for login

{
    "username": string,
    "password": string
}

```

## Logout api

To logout a user you have to send a get request with the token to the following link:

```bash

# Logout URL

https://albaqshi.bitregalo.com/api/logout/

# Header

{ headers: { Authorization: 'Token  ...........' } }

```

## Change Password

To change a user's passwords send a post request with headers and json to the fillowing link. Then you will get a valid response with token.

```bash


# Password change URL

https://albaqshi.bitregalo.com/api/change-password/

{ headers: { Authorization: 'Token  ...........' } }


# JSON for login

{
    "old_password": string,
    "new_password": string
}

```

## Profile

Get the profile info by sending a get request to the below link with the token in headers:

```bash


# Profile URL

https://albaqshi.bitregalo.com/api/profile/

{ headers: { Authorization: 'Token  ...........' } }

```
