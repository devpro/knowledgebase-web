---
title: "Logstash"
date: 2019-09-28T19:32:29+02:00
draft: true
---

## Configuration

### Plugins

Redis : [plugins-inputs-redis](https://www.elastic.co/guide/en/logstash/current/plugins-inputs-redis.html)

### HOW-TOs

#### Replace Timestamp by another field

```json
filter {
  date {
    match => ["@t", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSS'Z'"]
    target => "@timestamp"
  }
}
```

See [plugins-filters-date](https://www.elastic.co/guide/en/logstash/current/plugins-filters-date.html)

### Grok

- [grokdebug](https://grokdebug.herokuapp.com/)

### Examples

- [Logstash Configuration Examples](https://www.elastic.co/guide/en/logstash/current/config-examples.html)
