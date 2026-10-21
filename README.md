# Audit Contracts

This repository provides the Go module used by the WorkHub services to share the audit gRPC contract.

## Purpose

It centralizes the generated Go bindings and package metadata used by both the backend API and the audit-service implementation.

## Structure

- api/proto: generated or shared protocol buffer package content
- go.mod: module definition for the shared contract package

## Usage

Add it as a local replace dependency from sibling services:

```go
replace audit-contracts => ../audit-contracts
```

## CI

This repository is kept lean and is validated with a simple Go compile/test workflow on push and pull requests.

## Notes

Any API changes must be reflected in the source .proto contract and propagated to the consuming services before deployment.
