# VdotWorkout Object

## Description
This documentation provides information about the `VdotWorkout` model, which represents a workout event with given steps provided. Steps array contains elements that may have different model indicated by the `type` field.



| Property    | Type                             | Description                             |
|-------------|----------------------------------|-----------------------------------------|
| eventId     | string                           | Identifier of the event.                |
| eventName   | string                           | Name of the event.                      |
| eventDate   | string                           | Date and time of the event.             |
| eventType   | [EventType](../enums/eventtype.md)               | Type of the event.                      |
| eventStatus | [EventStatus](../enums/eventstatus.md)              | Status of the event.                    |
| steps       | Array of objects of type [WorkoutStep](workout-step.md) or [WorkoutRepeatStep](workout-repeat-step.md) | Collection of workout steps for the event. Each object in array represents a speficic workout step type, indicated by the `type` field. Possible types: [WorkoutStep](workout-step.md) or [WorkoutRepeatStep](workout-repeat-step.md)|

#### Sample response
<details>  

```json
{
    "eventId": "78edbf80-30ef-40ba-ac93-d8661ebb2b49",
    "eventName": "Quality Session",
    "eventDate": "2024-03-29T00:00:00",
    "eventType": "qualitySession",
    "status": "planned",
    "steps": [
        {
            "type": "step",
            "intensity": "warmup",
            "duration": {
                "type": "distance",
                "value": 1609.0
            },
            "target": null,
            "strokeType": null,
            "equipment": null,
            "excerciseCategory": null,
            "excerciseName": null,
            "weight": null,
            "order": 1
        },
        {
            "type": "repeatStep",
            "repeat": {
                "type": "untilStepsCompleted",
                "value": 4.0
            },
            "steps": [
                {
                    "type": "step",
                    "intensity": "interval",
                    "duration": {
                        "type": "distance",
                        "value": 400.0
                    },
                    "target": {
                        "type": "speed",
                        "value": null,
                        "valueLow": 4.6121087074279785,
                        "valueHigh": 4.819277286529541
                    },
                    "strokeType": null,
                    "equipment": null,
                    "excerciseCategory": null,
                    "excerciseName": null,
                    "weight": null,
                    "order": 2
                },
                {
                    "type": "step",
                    "intensity": "recovery",
                    "duration": {
                        "type": "distance",
                        "value": 400.0
                    },
                    "target": null,
                    "strokeType": null,
                    "equipment": null,
                    "excerciseCategory": null,
                    "excerciseName": null,
                    "weight": null,
                    "order": 3
                }
            ],
            "order": 4
        },
        {
            "type": "repeatStep",
            "repeat": {
                "type": "untilStepsCompleted",
                "value": 3.0
            },
            "steps": [
                {
                    "type": "step",
                    "intensity": "interval",
                    "duration": {
                        "type": "distance",
                        "value": 300.0
                    },
                    "target": {
                        "type": "speed",
                        "value": null,
                        "valueLow": 5.1023731231689453,
                        "valueHigh": 5.3571429252624512
                    },
                    "strokeType": null,
                    "equipment": null,
                    "excerciseCategory": null,
                    "excerciseName": null,
                    "weight": null,
                    "order": 5
                },
                {
                    "type": "step",
                    "intensity": "recovery",
                    "duration": {
                        "type": "distance",
                        "value": 300.0
                    },
                    "target": null,
                    "strokeType": null,
                    "equipment": null,
                    "excerciseCategory": null,
                    "excerciseName": null,
                    "weight": null,
                    "order": 6
                }
            ],
            "order": 7
        },
        {
            "type": "step",
            "intensity": "cooldown",
            "duration": {
                "type": "distance",
                "value": 1609.0
            },
            "target": null,
            "strokeType": null,
            "equipment": null,
            "excerciseCategory": null,
            "excerciseName": null,
            "weight": null,
            "order": 8
        }
    ]
}

```
</details>
