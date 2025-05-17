# nuclei-templates

## Cheatsheet

```
jq -r '{"ip":.ip_str, "port": .port} | join(":")' private/shodan/todo.json | ~/go/bin/nuclei -fhr -t todo.yaml -o private/log/todo.log
```