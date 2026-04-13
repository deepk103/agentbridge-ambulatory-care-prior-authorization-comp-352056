# Architecture Documentation

## Overview
This Plan-Execute implements Ambulatory Care Prior Authorization Compliance Checker for Healthcare & Life Sciences use cases.

## Components
1. **Signal Intake**: Collect, validate and normalize admission notes from LIS; attach a runId and timestamp for traceability.
2. **Plan**: Execute plan phase for the Plan-Execute pattern: persist interim state, enforce guardrails, and emit structured JSON results.
3. **Execute**: Execute execute phase for the Plan-Execute pattern: persist interim state, enforce guardrails, and emit structured JSON results.
4. **Plan Drafting**: Plan Drafting across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
5. **Risk Scoring**: Risk Scoring across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
6. **Triage**: Triage across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
7. **Outcome Measurement**: Assemble final payload with status, artifacts, KPIs and audit trail; store to HIE; return response JSON for the client.

## Data Flow
- Input: Signal Intake
- Processing: 7 sequential steps
- Output: Outcome Measurement
