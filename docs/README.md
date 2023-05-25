# ck9/cve_searchsploit-api

## About

Web API of [andreafioraldi/cve_searchsploit](https://github.com/andreafioraldi/cve_searchsploit)

I update mapping.json daily and provide it as WEB API hosted on GitHub Pages.

## Endpoints

### EDB-ID => CVE-ID

GET [https://ck9.github.io/cve_searchsploit-api/v1/exploitdb_mapping.json](https://ck9.github.io/cve_searchsploit-api/v1/exploitdb_mapping.json)

```json
{
  "9": [
    "CVE-2003-0132"
  ],
  "11": [
    "CVE-2003-0132"
  ],
  "13": [],
  "17": [],
  "22": [
    "CVE-2003-0276"
  ],
```

### CVE-ID => EDB-ID

GET [https://ck9.github.io/cve_searchsploit-api/v1/exploitdb_mapping_cve.json](https://ck9.github.io/cve_searchsploit-api/v1/exploitdb_mapping_cve.json)

```json
{
  "CVE-2003-0132": [
    "9",
    "11"
  ],
  "CVE-2003-0276": [
    "22",
    "22587"
  ],
  "CVE-2003-0226": [
    "35",
    "22670"
  ],
  "CVE-2003-0245": [
    "38"
  ],
  "CVE-2003-0567": [
    "59",
    "60",
    "62"
  ],
```

## Licence
[andreafioraldi/cve_searchsploit](https://github.com/andreafioraldi/cve_searchsploit)
