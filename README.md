# cve_searchsploit-api

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

___

# CVE SearchSploit

> version 1.7

Search an exploit in the local exploitdb database by its CVE.

Here you can get a free cve to exploit-db mapping in json format.

## Install

#### from PyPI

```
$ pip3 install cve_searchsploit
```

#### from GitHub

```
$ git clone https://github.com/andreafioraldi/cve_searchsploit
$ cd cve_searchsploit
$ python3 setup.py install
```

#### Requirements

+ python3
+ requests
+ progressbar2
+ git

## Usage
```
$ cve_searchsploit [parameters...]
```

#### Parameters
+  ```<cve>```                      search exploits by a cve
+  ```-u```                         update the cve-edbid mapping
+  ```-f <file with cve list>```    search exploits by a cve list file
+  ```-n <nessus csv scan file>```  search exploits by the cve matching with a nessus scan in csv format

### As a library

```python
>>> import cve_searchsploit as CS
>>> 
>>> CS.update_db()
Refreshing exploit-database repo with lastest exploits
From https://github.com/offensive-security/exploit-database
 * branch                master     -> FETCH_HEAD
Already up to date.
Refreshing EDBID-CVE mapping
100% (41823 of 41823) |##############| Elapsed Time: 0:00:00 Time:  0:00:00
>>> 
>>> CS.edbid_from_cve("CVE-2019-0708")
[46946, 47120, 47416]
>>> CS.cve_from_edbid(47120)
['CVE-2019-0708']
```

## Cite

If you use this tool in your academic work you can cite it using

```bibtex
@Misc{cve_searchsploit,
  author       = {Andrea Fioraldi},
  howpublished = {GitHub},
  month        = jun,
  title        = {{CVE SearchSploit}},
  year         = {2017},
  url          = {https://github.com/andreafioraldi/cve_searchsploit},
}
```
