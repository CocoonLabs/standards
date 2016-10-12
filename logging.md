## Logging

Logging standards and so on..



### Format

Application logs are expected to be serialized in JSON

```
blah blah
```



### Level

When in production, DEBUG \(10\) and levels lower that this will be suppressed.

In a non-production environment, one can turn on DEBUG \(10\) to view more information about what's going on.

| Level | Description |
| --- | --- |
| DEBUG \(10\) |  |
| INFO \(20\) |  |
| WARNING \(30\) |  |
| ERROR \(40\) |  |
| CRITICAL \(50\) |  |
| FATAL \(50\) |  |



### Streams

We are going to use the distinction of **stdout** and **stderr**.

| Stream | Purpose |
| --- | --- |
| stdout |  |
| stderr |  |



