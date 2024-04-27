## Workouts Get By Date Range

##### Endpoint
 <code>GET</code> <code>/api/v1/vdot-workouts/{fromDate}/{toDate}</code> Find complete workouts based on provided date range.

##### Required scope
> read:workouts

##### Authorization
> OAuth 2.0 [(documentation)](../OAuth.md)

##### Parameters

> | name      |  type     | data type               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | fromDate   |  required | string                  | The specific input in Date format (yyyy-MM-dd)  |
> | toDate     |  required | string                  | The specific input in Date format (yyyy-MM-dd) |

##### Limitations
Please note that difference between the from date and to date cannot be greater than 60 days.  \
'To date' has to be greater or equal to 'From date'.


##### Response codes

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `application/json`        | Successful response                                |
> | `401`         | `application/json`                | Bearer Token not valid or expired |
> | `404`         | `application/json`         | Event or User not found    |

##### Example cURL request

> ```javascript
>  curl -X GET -H "Content-Type: application/json" https://vdoto2.com/api/v1/vdot-workouts/2024-01-01/2024-02-25
>	-h "Authorization=Bearer dem6soGFEJYHHLgOzzbsyCN8Oj1TsshLWEdCnPlVwOKl8lqII9uoU2vNfLbkFImAcIGUaf1l-yGr3wCVxbhFrsjC7JGshXZPnI34u44VvH1u_j0czs_IEt5J-c_puXA53xxQ-Y0ZZuLOu3dX18xFL27jClc0_GZPMcOfMMgvAkulX7YTPALZVq6QhCDxqcLzPLg29gNsFDEIDOTERQeiD0H8H701fyxavsETnziDEztSoWtc_FFI_sklritftE_X9LtLYAMDQ70paxUpY-3ZUA" \
> ```

##### Response Model

An array of VdotWorkout models, see [VdotWorkout](../objects/workout-model.md) object reference for a complete list of properties.

##### Sample response

<details>

```json
[
    {
        "eventId": "daa61499-4eb6-40c6-b89a-8e35cbad1450",
        "eventName": "Easy Run",
        "eventDate": "2024-01-30T00:00:00",
        "eventType": "easyPace",
        "status": "completed",
        "steps": [
            {
                "type": "step",
                "intensity": "interval",
                "duration": {
                    "type": "distance",
                    "value": 3223.0
                },
                "target": {
                    "type": "speed",
                    "value": null,
                    "valueLow": 3.1198868751525879,
                    "valueHigh": 3.4387447834014893
                },
                "order": 0
            }
        ]
    },
    {
        "eventId": "7465e778-3116-4aaf-b309-4ab7472fbffd",
        "eventName": "Easy Run",
        "eventDate": "2024-03-10T00:00:00",
        "eventType": "easyPace",
        "status": "planned",
        "steps": [
            {
                "type": "step",
                "intensity": "interval",
                "duration": {
                    "type": "distance",
                    "value": 9656.0
                },
                "target": {
                    "type": "speed",
                    "value": null,
                    "valueLow": 3.1198868751525879,
                    "valueHigh": 3.4387447834014893
                },
                "order": 0
            }
        ]
    }     
]

```
</details>
