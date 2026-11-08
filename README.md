# Act-On MCP setup and connection checker

Generate Act-On MCP client configuration, inspect available tools and validate hosted endpoint access through PipMCP.

Maintainer: jannikco · License: MIT · Verification: **mock-only**

## Quick start

Requires Node.js 22 or later.

```sh
npm ci
npm test
npm start
```

The default example runs locally without credentials and makes no external changes. Verification status describes recorded evidence; local configuration tests do not establish that provider authentication or execution works.

## Connect act-on

[Create or sign in to PipMCP](https://pipmcp.com/register?app=act-on&utm_source=github&utm_campaign=github-act-on-mcp) and select the integration. Connect your authorized provider account and copy its hosted MCP endpoint. Set PIPMCP_ENDPOINT and, if required, PIPMCP_TOKEN in your environment. Run npm start to produce client configuration; run npm start -- --live for a read-only connection check. Provider app presence is catalog evidence, not live verification.

## Managed service

[Continue with PipMCP](https://pipmcp.com/register?app=act-on&utm_source=github&utm_campaign=github-act-on-mcp). This repository is maintained by the integration team and does not imply endorsement by LinkedIn or other providers.

## Provenance and support

Source revision: 2e150221c618f118effcbca5607ff44ea5ae63fd280b7bc32cb5a82aa91b89e9. The complete manifest is in integration.json; SHA256SUMS covers the reviewed artifact. Open a repository issue without credentials or personal data. See SECURITY.md for sensitive reports. No telemetry is sent by this code; signup links include explicit campaign parameters.

## Provider setup inventory

Run `npm start -- --setup` to inspect this app's recorded authentication requirements and setup links offline. Credentials are entered in PipMCP; this repository lists required field names only.

```json
{
  "type": "token_exchange",
  "requiredCredentialFields": [
    "provider_exchange_credentials"
  ],
  "requiredHeaderNames": [],
  "helpUrl": "https://developer.act-on.com/reference/grant-type-password",
  "tenantRequired": false,
  "accountParameterNames": [
    "account_id"
  ]
}
```

Provider documentation: https://developer.act-on.com/reference
Provider website: https://act-on.com/
