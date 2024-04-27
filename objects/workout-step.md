# WorkoutStep Object

## Description
This documentation provides information about the `WorkoutStep` model, which represents a step within a workout.

## Model Properties

| Property          | Type                                                  | Description                                                    |
|-------------------|-------------------------------------------------------|----------------------------------------------------------------|
| type              | [StepType](../enums/steptype.md)        | The type of the workout step. This property is always set to `Step`. |
| intensity         | [IntensityType](../enums/intensity.md)  | The intensity level of the workout step.                      |
| duration          | [Duration](duration.md)                                         | The duration of the workout step.                             |
| target            | [Target](target.md)                           | The target of the workout step.                               |
| order             | number | The order of the workout step within the workout sequence. |
### Example

```json
{
  "type": "step",
  "intensity": "cooldown",
  "duration": {
    "type": "distance",
    "value": 1609
  },
  "target": {
    "type": "speed",
    "value": 10,
    "valueLow": 5,
    "valueHigh": 15
  },
  "order": 8
}
```