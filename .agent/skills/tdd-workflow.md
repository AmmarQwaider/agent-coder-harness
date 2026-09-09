# TDD Workflow

When implementing new features or fixing complex logic, you must follow the Test-Driven Development (TDD) loop:

1. **Red (Write the Test)**: 
   - Based on the requirements, write a failing unit or integration test that defines the expected behavior.
   - Run the test to confirm it fails exactly as expected. Do not write the implementation code yet.
2. **Green (Make it Pass)**:
   - Write the simplest, most straightforward code necessary to make the test pass.
   - Run the test suite to confirm the new test passes without breaking existing tests.
3. **Refactor**:
   - Review the newly written code and the test.
   - Clean up the code, apply DRY principles, optimize, and ensure it aligns with the project's architectural standards.
   - Run the test suite again to confirm the refactoring did not break anything.
