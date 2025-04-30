# TODO

## favicon-detect.yaml

```yaml
- type: dsl
  name: "iqmessenger"
  dsl:
    - "status_code==200 && (\"1033082340\" == mmh3(base64_py(body)))"

- type: dsl
  name: "topdesk"
  dsl:
    - "status_code==200 && (\"-1177777311\" == mmh3(base64_py(body)))"

- type: dsl
  name: "schneider-electric"
  dsl:
    - "status_code==200 && (\"-139383140\" == mmh3(base64_py(body)))"

- type: dsl
  name: "usergate"
  dsl:
    - "status_code==200 && (\"-782553370\" == mmh3(base64_py(body)))"

- type: dsl
  name: "sonatype-nexus-repository-manager"
  dsl:
    - "status_code==200 && (\"1323738809\" == mmh3(base64_py(body)))"

- type: dsl
  name: "mikrotik-routeros"
  dsl:
    - "status_code==200 && (\"-1757562887\" == mmh3(base64_py(body)))"

- type: dsl
  name: "fastpanel-hosting"
  dsl:
    - "status_code==200 && (\"-1294748862\" == mmh3(base64_py(body)))"

- type: dsl
  name: "oracle-rest-data-services"
  dsl:
    - "status_code==200 && (\"1792417660\" == mmh3(base64_py(body)))"
```

## fingerprinthub-web-fingerprints.yaml

```
- type: word
  part: header
  name: sagecom-tr069
  words:
    - 'Www-Authenticate: Basic realm="Sagemcom TR-069"'
  case-insensitive: true

- type: word
  part: body
  name: fastpanel
  words:
    - '<title>FASTPANEL</title>'
  case-insensitive: true
```