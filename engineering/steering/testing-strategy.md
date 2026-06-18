# Testing Strategy

Design effective test strategies by balancing coverage, speed, and maintenance cost.

## Testing Pyramid

```text
        /  E2E  \         Few, slow, high confidence
       / Integration \    Some, medium speed
      /  Unit Tests   \   Many, fast, focused
```

## Strategy By Component Type

- API endpoints: unit tests for business logic, integration tests for the HTTP layer, contract tests for consumers
- Data pipelines: input validation, transformation correctness, idempotency tests
- Frontend: component tests, interaction tests, visual regression, accessibility
- Infrastructure: smoke tests, chaos experiments, load tests

## What To Cover

Focus on business-critical paths, error handling, edge cases, security boundaries, and data integrity.

Skip trivial getters and setters, framework internals, and one-off scripts unless they are operationally critical.

## Output

Produce a test plan that includes:

- what to test
- the test type for each area
- coverage targets
- example test cases
- gaps in existing coverage
