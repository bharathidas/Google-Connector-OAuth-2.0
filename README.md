# Google OAuth 2.0

Using Google OAuth 2.0, this module helps in generating access tokens and refresh tokens with Client ID and Client Secret.

•	Access Token - It can be used with any of the Google APIs, such as the Google Drive API. 
•	Refresh Token - Once the access token has expired, it will be used to generate a new one.

## Dependencies
•	Mendix modeler 9.12.4.
•	Encryption module
•	Community Commons Module
•	Nanoflow Commons Module

## Configuration
Setup Client ID and Client Secret in Google

https://developers.google.com/identity/gsi/web/guides/get-google-api-clientid

Configure ‘GoogleOAuthSettings_Overview’ to your Navigation.

## Generate Token:

Add the following information in ‘GoogleOAuthSettings_Overview’ page new button
1.	OAuth Name
2.	Client ID
3.	Client Secret
4.	Scope

Save your configuration and click on ‘Generate Token’ button to generate the token using OAuth2.0 Authorization.

The access token and refresh token will be obtained, encrypted, and stored once the authorization has been successful.
When the access token expires, the scheduler "SCE RefreshToken" will automatically generate a fresh token.

## Refresh Token Manually:

To Refresh the token manually, the user can click on Edit button in ‘GoogleOAuthSettings_Overview’ where the below details can be seen.

1.	OAuth Name

2.	Client ID

3.	Client Secret

4.	Scope

5.	Access Token

6.	Refresh Token

7.	Token Expire Date&Time

To regenerate the Access token, click ‘Refresh token’.

## Revoke Access:

If the Google OAuth access needs to be revoked for the configured OAuth Setting, click on ‘Revoke Access’ button to revoke the OAuth access. The access token and refresh token should be regenerated using the ‘Generate Token’ button after the OAuth access has been revoked.

## Reference:
https://developers.google.com/identity/protocols/oauth2/web-server

![Screenshot_1](https://user-images.githubusercontent.com/23263603/221199499-610c3b3b-7901-4500-9efd-ce05f516c194.png)

#### New OAuth Configuration:

![Screenshot_2](https://user-images.githubusercontent.com/23263603/221199515-11372762-9874-4b82-96ee-635dc3fabb9a.png)

#### Edit OAuth Configuration:

![Screenshot_3](https://user-images.githubusercontent.com/23263603/221199526-27c71215-329b-4ac3-9dd4-788b7bb51d11.png)

![Screenshot_4](https://user-images.githubusercontent.com/23263603/221199537-f0e9672a-bb50-4336-8365-d82d939f3945.png)

#### Refresh Token:

![Screenshot_5](https://user-images.githubusercontent.com/23263603/221199663-81a629ce-e9fc-410f-9155-c259fabb5e88.png)

