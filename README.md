# Robotframework Action
Run tests within the robot framework


## Example Workflow
```
name: Deploy to Cloud Foundry with Zero-Downtime-Plugin "Puppeteer"

on: [push]

jobs:
  test:
    runs-on: ubuntu-18.04
    
    steps:
    - name: Checkout Repository
      uses: actions/checkout@v2
    - name: Run Robot Tests
      uses: codefour-gmbh/robotframework-action@master
      env:
        ROBOT_TESTS: ${{ github.workspace }}/src/tests/robot
        ROBOT_REPORTS: ${{ github.workspace }}/reports
        SERVER_URL: https://some.domain.passed.as.environment
        SECRET: ${{ secrets.MY_SECRET_ENV_VAR }}
```
