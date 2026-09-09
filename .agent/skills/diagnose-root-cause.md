# Root Cause Diagnosis Framework

When tasked with debugging or fixing an issue, you must prove the bug's origin before proposing a fix. Follow these steps:

1. **Reproduce & Isolate**:
   - Understand exactly how to reproduce the issue.
   - Identify the specific file(s) and function(s) involved.
2. **Hypothesize**:
   - Formulate a clear hypothesis about why the bug is occurring based on the symptoms.
3. **Verify**:
   - Gather evidence to prove or disprove the hypothesis. This may involve adding temporary logging, running specific tests, or analyzing the data flow.
   - You MUST find the exact line(s) of code responsible.
4. **Propose Fix**:
   - Only after the root cause is irrefutably identified, propose a minimal, targeted fix.
   - Explain why the fix addresses the root cause and not just the symptom.
