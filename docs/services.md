# Services

## battery_notes.set_battery_replaced

For updating the [battery replaced date](./entities.md#battery-replaced). This allows you to change the date a battery was replaced.

See how to use this service in the [community contributions](./community.md)

| Parameter                | Optional | Description                                                                                                           |
| ------------------------ | -------- | --------------------------------------------------------------------------------------------------------------------- |
| `data.device_id`      | `no`    | The device id that you want to change the battery replaced date for. |
| `data.datetime_replaced` | `yes`    | The optional datetime that you want to set the battery replaced to, if omitted the current date/time will be used. |

## battery_notes.check_battery_last_reported (Beta Only)

For raising events for devices that haven't reported their battery level.  

The service will raise a seperate [battery_not_reported](./events/battery_not_reported) event for each device where its last reported date is older than the number of days specified.  

You can use this service call to schedule checks on batteries that is convenient to you, e.g. when you wake up, once a week etc.  

See how to use this service in the [community contributions](./community.md)

| Parameter                | Optional | Description                                                                                                           |
| ------------------------ | -------- | --------------------------------------------------------------------------------------------------------------------- |
| `data.days`      | `no`    |  The number of days since a device last reported its battery level. |
