# nuclei-templates

## Cheatsheet

```bash
jq -r '{"ip":.ip_str, "port": .port} | join(":")' shodan/todo.json
jq -r .link fofa/2025-10-26-wsus-known-ports-nl.json
nuclei -fhr -t ../nuclei-templates/drafts/todo.yaml -o log/date-todo.log
```

## Other fingerprints

- `http.html_hash:-1774716666`, Panasonic i-Pro Network Disk Recorder, `/cgi-bin/start.cgi`
- `http.favicon.hash:-47597126`, DedeCMS
- `http.html:"data-xwiki"`, `http.favicon.hash:831700033`, XWiki, extract version from / `\"xwikiplatformversion\">\s*<a[^>]+>\s*([\w\d\s\.\-]+)<\/a>`
- `http.favicon.hash:-1053531639`, Versa Networks

- Extraction version from MikoPBX from `var globalPBXVersion = '2024.1.114';`