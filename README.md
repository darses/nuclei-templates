# nuclei-templates

## Cheatsheet

```bash
jq -r '{"ip":.ip_str, "port": .port} | join(":")' private/shodan/todo.json | ~/go/bin/nuclei -fhr -t todo.yaml -o private/log/todo.log
```

## Nuclei DSL

To compare dates use: `to_number(unix_timestamp) < to_number(to_unix_time('2024-01-29'))`.
