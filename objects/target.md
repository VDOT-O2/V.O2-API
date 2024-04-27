# Target Object

## Description
This documentation provides information about the `Target` class, which represents a target in a workout.

## Model Properties

| Property   | Type               | Description                                       |
|------------|--------------------|---------------------------------------------------|
| type       | [TargetType](../enums/target.md) | The type of target.                               |
| value      | number             | The value associated with the target.             |
| valueLow   | number             | The low range value associated with the target.   |
| valueHigh  | number             | The high range value associated with the target.  |



## Example
```json
{
  "type": "speed",
  "value": 5.0,
  "valueLow": 3.0,
  "valueHigh": 7.0
}