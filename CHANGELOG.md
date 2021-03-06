# CHANGELOG

All notable changes to this project will be documented in this file.

### [Unreleased]

### [0.3.3] - 2016-05-03

##### Fixed
- Important bug with PKCE and form submit in Auth Request.

### [0.3.2] - 2016-04-26

##### Added
- Choose type of client on creation.
- Implement Proof Key for Code Exchange by OAuth Public Clients.
- Support for prompt parameter.
- Support for different client JWT tokens algorithm.

##### Fixed
- Not auto-approve requests for non-confidential clients (publics).

### [0.3.1] - 2016-03-09

##### Fixed
- response_type was not being validated (OpenID request).

### [0.3.0] - 2016-02-23

##### Added
- Support OAuth2 requests.
- Decorator for protecting views with OAuth2.
- Setting OIDC_IDTOKEN_PROCESSING_HOOK.

### [0.2.5] - 2016-02-03

##### Added
- Setting OIDC_SKIP_CONSENT_ALWAYS.

##### Changed
- Removing OIDC_RSA_KEY_FOLDER setting. Moving RSA Keys to the database.
- Update pyjwkest to version 1.1.0.

##### Fixed
- Nonce parameter missing on the decide form.
- Set Allow-Origin header to jwks endpoint.

### [0.2.4] - 2016-01-20

##### Added
- Auto-generation of client ID and SECRET using the admin.
- Validate nonce parameter when using Implicit Flow.

##### Fixed
- Fixed generating RSA key by ignoring value of OIDC_RSA_KEY_FOLDER.
- Make OIDC_AFTER_USERLOGIN_HOOK and OIDC_IDTOKEN_SUB_GENERATOR to be lazy imported by the location of the function.
- Problem with a function that generate urls for the /.well-known/openid-configuration/ endpoint.

### [0.2.3] - 2016-01-06

##### Added
- Make user and client unique on UserConsent model.
- Support for URL's without end slash.

##### Changed
- Upgrade pyjwkest to version 1.0.8.

##### Fixed
- String format error in models.
- Redirect to non http urls fail (for Mobile Apps).

### [0.2.1] - 2015-10-21

##### Added
- Refresh token flow.

##### Changed
- Upgrade pyjwkest to version >= 1.0.6.

##### Fixed
- Unicode error in Client model.
- Bug in creatersakey command (when using Python 3).
- Bug when updating pyjwkest version.

### [0.2.0] - 2015-09-25

##### Changed
- UserInfo model was removed. Now you can add your own model using OIDC_USERINFO setting.

##### Fixed
- ID token does NOT contain kid.

### [0.1.2] - 2015-08-04

##### Added
- Add token_endpoint_auth_methods_supported to discovery.

##### Fixed
- Missing commands folder in setup file.

### [0.1.1] - 2015-07-31

##### Added
- Sending access_token as query string parameter in UserInfo Endpoint.
- Support HTTP Basic client authentication.

##### Changed
- Use models setting instead of User.

##### Fixed
- In python 2: "aud" and "nonce" parameters didn't appear in id_token.

### [0.1.0] - 2015-07-17

##### Added
- Now id tokens are signed/encrypted with RS256.
- Command for easily generate random RSA key.
- Jwks uri to discovery endpoint.
- id_token_signing_alg_values_supported to discovery endpoint.

##### Fixed
- Nonce support for both Code and Implicit flow.

### [0.0.7] - 2015-07-06

##### Added
- Support for Python 3.
- Way of remember user consent and skipt it (OIDC_SKIP_CONSENT_ENABLE).
- Setting OIDC_SKIP_CONSENT_EXPIRE.

##### Changed
- Now OIDC_EXTRA_SCOPE_CLAIMS must be a string, to be lazy imported.

### [0.0.6] - 2015-06-16

##### Added
- Better naming for models in the admin.

##### Changed
- Now tests run without the need of a project configured.

##### Fixed
- Error when returning address_formatted claim.

### [0.0.5] - 2015-05-09

##### Added
- Support for Django 1.8.

##### Fixed
- Validation of scope in UserInfo endpoint.

### [0.0.4] - 2015-04-22

##### Added
- Initial migrations.

##### Fixed
- Important bug with id_token when using implicit flow.
- Validate Code expiration in Auth Code Flow.
- Validate Access Token expiration in UserInfo endpoint.

### [0.0.3] - 2015-04-15

##### Added
- Normalize gender field in UserInfo.

##### Changed
- Make address_formatted a property inside UserInfo.

##### Fixed
- Important bug in claims response.

### [0.0.2] - 2015-03-26

##### Added
- Setting OIDC_AFTER_USERLOGIN_HOOK.

##### Fixed
- Tests failing because an incorrect tag in one template.

### [0.0.1] - 2015-03-13

##### Added
- Provider Configuration Information endpoint.
- Setting OIDC_IDTOKEN_SUB_GENERATOR.

##### Changed
- Now use setup in OIDC_EXTRA_SCOPE_CLAIMS setting.

### [0.0.0] - 2015-02-26
