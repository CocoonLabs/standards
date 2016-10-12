## Logging

This document describes how we write program logs.

Our standards were inspired by [https:\/\/12factor.net\/logs](https://12factor.net/logs)

### Format

Format is in modified ELF.

Application logs data are expected to be serialized in JSON.

```
2010-05-02 15:42:15 '{"host": "0.0.0.0", "port": "3000"}'
```

### Level

When in production, DEBUG \(10\) and levels lower that this will be suppressed.

In a non-production environment, one can turn on DEBUG \(10\) to view more information about what's going on.

| Level | Description |
| --- | --- |
| DEBUG \(10\) | System events. Verbose internal calls. |
| INFO \(20\) | High-level events. Verbose internal calls. |
| WARNING \(30\) | Non-error exceptions log \(page 404, failed transaction, etc\). |
| ERROR \(40\) | Unhandled exceptions. No system impact. |
| CRITICAL \(50\) | Unhandled exception. System will shutdown soon. |
| FATAL \(50\) | Unhandled exception. System shutdown. |

### Streams

We are going to use the distinction of **stdout** and **stderr**.

| Stream | Purpose |
| --- | --- |
| stdout | Primary program output \(script result, etc\) |
| stderr | Secondary program output \(logs, etc\) |

