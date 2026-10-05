# twtty-oidc-smoketest

Throwaway repo to validate GitHub OIDC → Azure user-assigned managed identity
federated login works with **no stored secrets**. Delete after the test.

The `oidc-smoke` workflow (manual trigger) runs `azure/login` using repo
**variables** (not secrets): `AZURE_CLIENT_ID`, `AZURE_TENANT_ID`,
`AZURE_SUBSCRIPTION_ID`. A green run proves the federated credential authenticates
the workflow as the UAMI.
