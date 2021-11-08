1. All workflows go to `.github/workflows`
2. Don't commit the workflow if the constructed project does not allow public distribution (check its license before committing)
3. All workflows should use the format
```yaml
name: <Your Workflow Name>

on:
  push:
    branches: [ main ]
    paths:
      - '.github/workflows/<your workflow file>.yml'
  schedule:
    - cron: '0 0 */3 * *'

jobs:
  # Your jobs here
```
