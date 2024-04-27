# RepeatStep Object

## Description
This documentation provides information about the `RepeatStep` class, which represents a repeat step within a workout.

## Model Properties

| Property      | Type               | Description                                              |
|---------------|--------------------|----------------------------------------------------------|
| type          | [RepeatType](../enums/repeat.md) | The type of repeat condition.                            |
| value         | number             | The value associated with the repeat condition.          |


## Example
```json
{
  "type": "untilTime",
  "value": 5.0
}
```

