# controller-schedules-platform

Platform-level schedules (drift detection, reconciliation)

## CasC Key

```
controller_schedules
```

## Usage

Place JSON files in this repository using the `controller_schedules` key.
The CasC dispatcher will automatically pick up and apply these configurations
to AAP when the CI/CD pipeline triggers.

### Example

```json
{
    "controller_schedules": [
        {
            "name": "example-resource",
            "description": "Replace with your actual configuration"
        }
    ]
}
```

## CI/CD Pipeline

This repository includes a thin CI/CD caller that triggers the platform's
shared CasC pipeline on push and pull request events. The pipeline validates
JSON files and triggers the dispatcher Job Template in AAP.

## Part of the Hybrid CasC Solution

This repository is managed by the **aap-casc-platform-demo** platform team as part
of the Hybrid AAP Configuration-as-Code framework. See the
[aap-casc-engine](../aap-casc-engine) repository
for full documentation.
