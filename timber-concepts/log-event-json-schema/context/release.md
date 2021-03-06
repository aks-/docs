# Release Context

*Note: This context is automatically added to your logs through our [libraries](/languages)*

The `release` context adds data about the current release (or deployment) of your application.

## Example JSON Structure


```json
{
  "context": {
    "http": {
      "commit_hash": "xf45j3kdk3k7l89j3jf",
      "created_at": "2017-01-01T01:02:23.432322Z",
      "version": "v2.1.2"
    }
  }
}
```

## Field descriptions

Name | Type | Description
-----|------|------------
`context.release.commit_hash` | `string` | The CVS commit hash for the current release. `optional`
`context.release.created_at` | `string` | When the release was created. `optional`
`context.release.version` | `string` | The version of the current release. `optional`

All fields are optional, but one must be supplied.


## Using this data

1. [Search it](/app/console/searching) with queries like: `release.version:1.2.1` or `has:release.version`
2. [Alert on it](/app/console/alerts) with threshold based alerts
3. [Graph & visualize it](/app/console/graphing)
4. [Access this data by viewing the log's metadata](/app/console/view-a-logs-metadata-context)

---

### Related Docs

1. [**Metadata, context, and events**](/concepts/metadata-context-and-events)
2. [**Timber libraries**](/languages)
