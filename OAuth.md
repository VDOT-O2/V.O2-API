# OAuth 2.0 - API Authentication and Authorization

* [Client Authentication](#client-authentication)

## Client Authentication
Clients must authenticate with client credentials (client ID and secret) when issuing requests to `/v1/oauth/token` endpoint. Basic HTTP authentication should be used

Please contact us by sending email to: info@vdoto2.com if you would like to be our API consumer.

## Grant Types

### Authorization code
The authorization code grant type is used to obtain both access tokens and refresh tokens and is optimized for confidential clients. Since this is a redirection-based flow, the client must be capable of interacting with the resource owner's user-agent (typically a web browser) and capable of receiving incoming requests (via redirection) from the authorization server.

The client initiates the flow by directing the resource owner's user-agent to the authorization endpoint. The client includes its client identifier, requested scope, local state, and a redirection URI to which the authorization server will send the user-agent back once access is granted (or denied).

`https://vdoto2.com/oauth/authorize?client_id=test_client_&redirect_uri=https%3A%2F%2Fvdoto2.com&response_type=code&scope=read:workouts`

The client requests an access token from the authorization server's token endpoint by including the authorization code received in the previous step. When making the request, the client authenticates with the authorization server. The client includes the redirection URI used to obtain the authorization code for verification.

```

curl --compressed -v https://vdoto2.com/oauth/token \
	-d client_id=your_client_id \
	-d client_secret=your_client_secret \
	-d "grant_type=authorization_code" \
	-d "code=7afb1c55-76e4-4c76-adb7-9d657cb47a27" \
	-d "redirect_uri=https://yourdomain.com"

```

The authorization server authenticates the client, validates the authorization code, and ensures that the redirection URI received matches the URI used to redirect the client before. If valid, the authorization server responds back with an access token and, optionally, a refresh token.

```json
{
  "access_token": "00ccd40e-72ca-4e79-a4b6-67c95e2e3f1c",
  "expires_in": 3600,
  "token_type": "Bearer",
  "refresh_token": "6fd8d272-375a-4d8a-8d0f-43367dc8b791"
}
```

### Refreshing an Access Token

The client can make a refresh request to the token endpoint in order to refresh the access token.

```
curl --compressed -v https://vdoto2.com/oauth/token \
	-u test_client_1:test_secret \
	-d "grant_type=refresh_token" \
	-d "refresh_token=6fd8d272-375a-4d8a-8d0f-43367dc8b791"
```