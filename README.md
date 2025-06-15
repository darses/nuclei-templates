# nuclei-templates

## Cheatsheet

```bash
jq -r '{"ip":.ip_str, "port": .port} | join(":")' private/shodan/todo.json | ~/go/bin/nuclei -fhr -t todo.yaml -o private/log/todo.log
```

## Nuclei DSL

To compare dates use: `to_number(unix_timestamp) < to_number(to_unix_time('2024-01-29'))`.

## Other favicons

- `http.favicon.hash:-1403225937` NightC2 (Botnet C2 panel)
- `http.favicon.hash:-857956556` "SiteManager"

## Other fingerprints

- `http.html_hash:-1774716666`, Panasonic i-Pro Network Disk Recorder, `/cgi-bin/start.cgi`
- `http.favicon.hash:-47597126`, DedeCMS
- `http.html:"data-xwiki"`, `http.favicon.hash:831700033`, XWiki, extract version from / `\"xwikiplatformversion\">\s*<a[^>]+>\s*([\w\d\s\.\-]+)<\/a>`
