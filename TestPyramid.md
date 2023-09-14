# Test Pyramid

## Objective

A test pyramid is a visualization of the different levels and types of tests in a software testing strategy, arranged in the shape of a pyramid to represent the distribution and priorities of these tests. Here's a test pyramid for The Road Warrior:

![TestPyramid](.media/TestPyramid.png)

### Unit Tests

* Scope: Individual functions, methods, or components.
* Characteristics:
  * High volume: Many unit tests covering various code paths.
  * Fast execution: These tests should execute quickly.
  * Isolated: Tests are isolated from external dependencies.
* Purpose: To verify the correctness of small code units in isolation.

### Integration Tests

* Scope: Interactions between different services, or components.
* Characteristics:
  * Moderate volume: Fewer integration tests compared to unit tests.
  * Medium execution time: Integration tests may involve more complex scenarios.
  * Realistic: Tests reflect how different parts of the system interact.
* Purpose: To validate that integrated components work together as expected.

### End-to-End (E2E) Tests

* Scope: The entire application from the user's perspective.
* Characteristics:
  * Few in number: E2E tests are typically the fewest in number.
  * Slow execution: These tests mimic real user interactions and may involve UI automation.
  * Realistic: Tests simulate actual user journeys.
* Purpose: To ensure that the complete application functions correctly from a user's standpoint and that major user flows work as expected.
