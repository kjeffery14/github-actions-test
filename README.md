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
  "event_type": "build"
}
```

Send post request to repository endpoint:
https://api.github.com/${account}/${repository}/dispatches

Basic authentication with personal token (no username) 
