# nuclei-templates

## Cheatsheet

```bash
jq -r '{"ip":.ip_str, "port": .port} | join(":")' shodan/todo.json
jq -r .link fofa/2025-10-26-wsus-known-ports-nl.json
nuclei -fhr -t ../nuclei-templates/drafts/todo.yaml -o log/date-todo.log
```

## Nuclei DSL

To compare dates use: `to_number(unix_timestamp) < to_number(to_unix_time('2024-01-29'))`.

To convert last-m to unix.

```yaml
    extractors:
      - type: kval
        part: header
        kval:
          - last_modified
        name: last_modified_str
        internal: true

      - type: dsl
        name: unix_timestamp
        dsl:
          - 'to_unix_time(last_modified_str, "Mon, 02 Jan 2006 15:04:05 GMT")'
```

## Other fingerprints

- `http.html_hash:-1774716666`, Panasonic i-Pro Network Disk Recorder, `/cgi-bin/start.cgi`
- `http.favicon.hash:-47597126`, DedeCMS
- `http.html:"data-xwiki"`, `http.favicon.hash:831700033`, XWiki, extract version from / `\"xwikiplatformversion\">\s*<a[^>]+>\s*([\w\d\s\.\-]+)<\/a>`
- `http.favicon.hash:-1053531639`, Versa Networks

- Extraction version from MikoPBX from `var globalPBXVersion = '2024.1.114';`