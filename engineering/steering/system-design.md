# System Design

Design systems, services, and architectures with explicit assumptions and trade-offs.

## Framework

### 1. Requirements Gathering

- Functional requirements
- Non-functional requirements such as scale, latency, availability, and cost
- Constraints such as team size, timeline, or existing stack

### 2. High-Level Design

- Component diagram
- Data flow
- API contracts
- Storage choices

### 3. Deep Dive

- Data model design
- API style and endpoint design
- Caching strategy
- Queue and event design
- Error handling and retry logic

### 4. Scale And Reliability

- Load estimation
- Horizontal versus vertical scaling
- Failover and redundancy
- Monitoring and alerting

### 5. Trade-off Analysis

Make trade-offs explicit across complexity, cost, team familiarity, time to market, and maintainability.

## Output

Produce structured design documents with:

- clear assumptions
- diagrams in ASCII or prose
- trade-off analysis
- notes on what should be revisited as the system grows
