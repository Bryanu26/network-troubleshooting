# DoorBird and Altronix - NO/NC Relay Trigger Troubleshooting

## Environment

Door access system integrating a DoorBird intercom/door station with an Altronix power/access-control component.

## Symptoms

* The door-control trigger was not behaving as expected during integration.
* Wiring was present, but the relay logic did not produce the intended lock/door response.

## Troubleshooting

* Reviewed the trigger wiring between the DoorBird and Altronix equipment.
* Checked the relay contact behavior rather than treating the circuit as a simple powered output.
* Worked through the difference between Normally Open (NO) and Normally Closed (NC) relay logic.
* Verified the required trigger behavior for the connected access-control hardware.
* The final configuration was completed with assistance from a manager after the initial troubleshooting session.

## Root Cause

The integration depended on using the correct NO/NC relay logic for the trigger path.

## Solution

Configured the relay/trigger path according to the required NO/NC behavior and validated proper door-control operation.

## Lessons Learned

* Dry-contact relay outputs must be understood as logic states, not just voltage outputs.
* NO versus NC selection can completely change how access-control equipment behaves.
* Before changing hardware, verify the expected idle and triggered state of every relay in the signal path.
* Escalation is useful when the system architecture is unfamiliar; the important part is understanding the final fix and applying the lesson next time.
