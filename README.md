# The Complete GitHub Actions Course

1. Create new folder .github
2. Create workflows folder inside
3. Create simple.yml file for first workflow

## Repository Dispatch

Event definition:

```yaml
on:
  repository_dispatch:
    types:
    - build
```

Sample payload:

```json
{
  "event_type": "build",
  "client_payload": {
      "environment": "PROD"
  }
}
```

Send post request to repository endpoint:
https://api.github.com/${account}/${repository}/dispatches

Basic authentication with personal token (no username) 

Client payload will be available in ${{ github.event.client_payload.environment }} in workflow job.
