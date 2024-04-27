# WorkoutRepeatStep Object

## Description
This documentation provides information about the `WorkoutRepeatStep` model, which represents a repeat step within a workout.

## Model Properties

| Property | Type | Description |
|----------|------|-------------|
| type     | [RepeatType](../enums/repeat.md) | The type of the workout step. This property is always set to `RepeatStep`. |
| repeat   | [RepeatStep](repeat-step.md) | The configuration for the repeat step. |
| steps    | Array of objects of type [WorkoutStep](workout-step.md) or [WorkoutRepeatStep](../objects/workout-repeat-step.md) | Collection of workout steps for the event. Each object in array represents a speficic workout step type, indicated by the `type` field. Possible types: [WorkoutStep](workout-step.md) or [WorkoutRepeatStep](../objects/workout-repeat-step.md) |
| order    | number | The order of the workout step within the workout sequence. |
