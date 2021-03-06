# Custom Context

*Note: Our [libraries](/languages) provide a simple API to set custom contexts.*

The `custom` context allows you to extend beyond the context [already provided by Timber](/concepts/log-event-json-schema/context) by providing your own custom contexts.


## Example JSON Structure


```json
{
  "context": {
    "custom": {
      "application": {
        "id": 1234,
        "name": "ABC Production App"
      }
    }
  }
}
```

Notice the `application` key. This is your context type. Each custom context must contain a single root key that creates a namespace. This ensures a clean schema avoiding variable name and type conflicts.

## Using this data

1. [Search it](/app/console/searching) with queries like: `application.id:1234` or `has:application.id`
2. [Alert on it](/app/console/alerts) with threshold based alerts
3. [Graph & visualize it](/app/console/graphing)
4. [Access this data by viewing the log's metadata](/app/console/view-a-logs-metadata-context)

---

### Related Docs

1. [**Metadata, context, and events**](/concepts/metadata-context-and-events)
2. [**Timber libraries**](/languages)
