---
swagger: "2.0"
x-collection-name: AWS EC2 Systems Manager
x-complete: 0
info:
  title: Amazon EC2 Systems Manager API Get Automation Execution
  version: 1.0.0
  description: Get detailed information about a particular Automation execution.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeAutomationExecutions:
    get:
      summary: Describe Automation Executions
      description: Provides details about all active and terminated Automation executions.
      operationId: describeAutomationExecutions
      x-api-path-slug: actiondescribeautomationexecutions-get
      parameters:
      - in: query
        name: Filters
        description: Filters used to limit the scope of executions that are requested
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of items to return for this call
        type: string
      - in: query
        name: NextToken
        description: The token for the next set of items to return
        type: string
      responses:
        200:
          description: OK
      tags:
      - Automation
      - Executions
  /?Action=GetAutomationExecution:
    get:
      summary: Get Automation Execution
      description: Get detailed information about a particular Automation execution.
      operationId: getAutomationExecution
      x-api-path-slug: actiongetautomationexecution-get
      parameters:
      - in: query
        name: AutomationExecutionId
        description: The unique identifier for an existing automation execution to
          examine
        type: string
      responses:
        200:
          description: OK
      tags:
      - Automation
      - Execution
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---