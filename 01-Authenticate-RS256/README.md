# Hapi Authentication for RS256-Signed Tokens
<img src="https://img.shields.io/badge/community-driven-brightgreen.svg"/> <br>

This sample demonstrates how to protect endpoints in an Hapi API by verifying an incoming JWT access token signed by Auth0. The token must be signed with the RS256 algorithm and must be verified against your Auth0 JSON Web Key Set.

This repo is supported and maintained by Community Developers, not Auth0. For more information about different support levels check https://auth0.com/docs/support/matrix .

## Getting Started

If you haven't already done so, [sign up](https://auth0.com) for your free Auth0 account and create a new client in the [dashboard](https://manage.auth0.com).

You must ensure that the APIs section is enabled in your Auth0 dashboard. To do so, go to the [Advanced Settings](https://manage.auth0.com/#/account/advanced) area and verify that **Enable APIs Section** is switched on. Next, navigate to APIs in the sidebar and create a new API. The identifier for your API will be required later. 

Clone the repo or download it from the Hapi API quickstart page in Auth0's documentation.

### Installation

#### Setup the `.env` File

If you download this sample from the Hapi API quickstart page, a `.env` file will come pre-populated with your API identifier and Auth0 domain. If you clone the repo from GitHub, you will need to rename `.env.example` to `.env` and provide these values manually.

#### Install the Dependencies and Start the API

```bash
cd 01-Authenticate-RS256
npm install
npm start
```

The API will be served at `http://localhost:3010`.

## Usage

### Endpoints

The sample includes three endpoints:

**GET** /api/public
* An unprotected endpoint which returns a message on success. Does not require a valid JWT access token.

**GET** /api/private
* A protected endpoint which returns a message on success. Requires a valid JWT access token.

**GET** /api/private-scoped
* A protected endpoint which returns a message on success. Requires a valid JWT access token containing a `scope` of `read:messages`.

#### Running the Sample With Docker

In order to run the example with docker you need to have `docker` installed.

You also need to set the client credentials as explained [previously](#setup-the-env-file).

Execute in command line `sh exec.sh` to run the Docker in Linux, or `.\exec.ps1` to run the Docker in Windows.

## Contribute

Feel like contributing to this repo? We're glad to hear that! Before you start contributing please visit our [Contributing Guideline](https://github.com/auth0-community/getting-started/blob/master/CONTRIBUTION.md).

Here you can also find the [PR template](https://github.com/auth0-community/auth0-hapi-api-samples/blob/master/PULL_REQUEST_TEMPLATE.md) to fill once creating a PR. It will automatically appear once you open a pull request.

## Issues Reporting

Spotted a bug or any other kind of issue? We're just humans and we're always waiting for constructive feedback! Check our section on how to [report issues](https://github.com/auth0-community/getting-started/blob/master/CONTRIBUTION.md#issues)!

Here you can also find the [Issue template](https://github.com/auth0-community/auth0-hapi-api-samples/blob/master/ISSUE_TEMPLATE.md) to fill once opening a new issue. It will automatically appear once you create an issue.

## Repo Community

Feel like PRs and issues are not enough? Want to dive into further discussion about the tool? We created topics for each Auth0 Community repo so that you can join discussion on stack available on our repos. Here it is for this one: [auth0-hapi-api-samples](https://community.auth0.com/t/auth0-community-oss-auth0-hapi-api-samples/15975)

<a href="https://community.auth0.com/">
<img src="/Assets/join_auth0_community_badge.png"/>
</a>

## License

This project is licensed under the MIT license. See the [LICENSE](https://github.com/auth0-community/auth0-hapi-api-samples/blob/master/LICENSE) file for more info.

## What is Auth0?

Auth0 helps you to:

* Add authentication with [multiple authentication sources](https://docs.auth0.com/identityproviders), either social like
* Google
* Facebook
* Microsoft
* Linkedin
* GitHub
* Twitter
* Box
* Salesforce
* etc.

**or** enterprise identity systems like:
* Windows Azure AD
* Google Apps
* Active Directory
* ADFS
* Any SAML Identity Provider

* Add authentication through more traditional [username/password databases](https://docs.auth0.com/mysql-connection-tutorial)
* Add support for [linking different user accounts](https://docs.auth0.com/link-accounts) with the same user
* Support for generating signed [JSON Web Tokens](https://docs.auth0.com/jwt) to call your APIs and create user identity flow securely
* Analytics of how, when and where users are logging in
* Pull data from other sources and add it to user profile, through [JavaScript rules](https://docs.auth0.com/rules)

## Create a free Auth0 account

* Go to [Auth0 website](https://auth0.com/signup)
* Hit the **SIGN UP** button in the upper-right corner
