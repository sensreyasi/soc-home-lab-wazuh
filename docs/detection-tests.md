# Safe Detection Test Plan

**Status: NOT EXECUTED.** Fill in actual outcomes after running each exercise.

| ID | Test | Safe procedure | Expected observation | Actual result |
|---|---|---|---|---|
| SOC-01 | Agent connectivity | Start the enrolled agent and check its status | Agent shown as active | Not tested |
| SOC-02 | Failed authentication | Enter an incorrect password a few times on your own lab test account | Relevant auth events may appear if logging and rules are configured | Not tested |
| SOC-03 | Successful authentication | Sign in to your own lab test account | Login event visible if collected | Not tested |
| SOC-04 | File integrity | Enable file integrity monitoring for a dedicated test directory; create/edit a harmless text file | File change event after monitoring interval | Not tested |
| SOC-05 | Agent disconnect | Stop the agent service briefly and restore it | Agent status change / alert depending on configuration | Not tested |

## Evidence checklist
For each test record: date/time and timezone, VM OS, agent version, test steps, relevant rule ID, alert severity, screenshot filename, and analyst interpretation.

Do not fabricate alerts. A missing alert is a valid result: investigate whether the event was generated, collected, parsed, and matched by a rule.
