---
pcx_content_type: reference
title: Bitbucket Cloud
rss: file
---

# Bitbucket Cloud

{{<render file="casb/_integration-description.md" withParameters="Bitbucket Cloud;;Bitbucket Cloud account">}}

{{<Aside type="note">}}
The CASB integration for Confluence is currently only compatible with Confluence Cloud accounts.
{{</Aside>}}

## Integration prerequisites

- A Confluence Cloud plan (Free, Standard, Premium, Enterprise)

- Access to a Confluence Cloud account with Site admin and/or Organization admin permissions

## Integration permissions

For the Confluence Cloud integration to function, Cloudflare CASB requires the following permissions via an OAuth 2.0 app:

- `read:confluence-space.summary`
- `read:confluence-props`
- `read:confluence-content.all`
- `read:confluence-content.summary`
- `read:confluence-content.permission`
- `read:confluence-user`
- `read:confluence-groups`

These permissions follow the principle of least privilege to ensure that only the minimum required access is granted. To learn more about each permission, refer to the [Atlassian scopes documentation](https://developer.atlassian.com/cloud/confluence/scopes-for-oauth-2-3LO-and-forge-apps/).

## Security findings

{{<render file="casb/_security-findings.md" withParameters="Bitbucket Cloud;;atlassian-confluence">}}

### Access security

Flag user and third-party app access issues, including account misuse, sharing security, and users not following best practices.

| Finding                                               | Severity |
| ----------------------------------------------------- | -------- |
| Unknown or anonymous user with edit access to content | Critical |
| Unknown or anonymous user with edit access to space   | High     |
| External collaborators with content access            | Medium   |
| External collaborator with access                     | Medium   |
| Third-party app with edit access to space             | Medium   |
| Third-party app with edit access to content           | Medium   |
| External collaborators with edit access to space      | Medium   |
| External collaborators with edit access to content    | Medium   |
| Unknown or anonymous user with access                 | Low      |
| Third-party app with content access                   | Low      |