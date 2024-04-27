## Workout Get By Event ID

##### Endpoint
 <code>GET</code> <code>/api/v1/vdot-workouts/{eventId}</code> Find complete workout based on provided {eventId}.

##### Required scope
> read:workouts

##### Authorization
> OAuth 2.0 [(documentation)](../OAuth.md)

##### Parameters

> | name      |  type     | data type               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | eventId   |  required | string                  | The specific event unique identifier  |


##### Response codes

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `application/json`        | Successful response                                |
> | `401`         | `application/json`                | Bearer Token not valid or expired |
> | `404`         | `application/json`         | Event or User not found    |

##### Example cURL request

> ```javascript
>  curl -X GET -H "Content-Type: application/json" https://vdoto2.com/api/v1/vdot-workouts/06ab5c70-2ec3-401b-8b01-d33a9a4f0a1f
>	-h "Authorization=Bearer dem6soGFEJYHHLgOzzbsyCN8Oj1TsshLWEdCnPlVwOKl8lqII9uoU2vNfLbkFImAcIGUaf1l-yGr3wCVxbhFrsjC7JGshXZPnI34u44VvH1u_j0czs_IEt5J-c_puXA53xxQ-Y0ZZuLOu3dX18xFL27jClc0_GZPMcOfMMgvAkulX7YTPALZVq6QhCDxqcLzPLg29gNsFDEIDOTERQeiD0H8H701fyxavsETnziDEztSoWtc_FFI_sklritftE_X9LtLYAMDQ70paxUpY-3ZUA" \
> ```

##### Response Model

VdotWorkout model, see [VdotWorkout](../objects/workout-model.md) object reference for a complete list of properties.

##### Sample response

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
