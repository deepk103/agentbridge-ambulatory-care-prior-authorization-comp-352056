# API Documentation

## Endpoints
### Signal Intake
- **Description**: Collect, validate and normalize admission notes from LIS; attach a runId and timestamp for traceability.
- **Type**: Processing

### Plan
- **Description**: Execute plan phase for the Plan-Execute pattern: persist interim state, enforce guardrails, and emit structured JSON results.
- **Type**: Processing

### Execute
- **Description**: Execute execute phase for the Plan-Execute pattern: persist interim state, enforce guardrails, and emit structured JSON results.
- **Type**: Processing

### Plan Drafting
- **Description**: Plan Drafting across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Risk Scoring
- **Description**: Risk Scoring across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Triage
- **Description**: Triage across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Outcome Measurement
- **Description**: Assemble final payload with status, artifacts, KPIs and audit trail; store to HIE; return response JSON for the client.
- **Type**: Processing
