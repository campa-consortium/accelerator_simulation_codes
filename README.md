# 📙 Accelerator Simulation Codes
[![See List](https://img.shields.io/badge/see-list-brightgreen.svg)](https://campa-consortium.github.io/accelerator_simulation_codes/)

This is a community database of accelerator simulation codes.

Contributions to the file `codes.json`, in which we list accelerator simulation codes, are welcome!

## Keywords (Schema)

In order to parse the table efficiently, we apply a common schema.
Please use the following keywords for each entry in `codes.json`:


| Key                 | Required | Description                                                         |
|---------------------|----------|---------------------------------------------------------------------|
| `title`             | Yes      | Title of the code                                                   |
| `subtitle`          | No       | Subtitle of the code                                                |
| `description`       | Yes      | A short description (<=300 characters)                              |
| `application`       | No       | Keywords (tags): list of application areas                          |
| `compute`           | No       | Keywords (tags): list of computational features                     |
| `method`            | No       | Keywords (tags): list of mathematical models & numerical methods    |
| `phenomena`         | No       | Keywords (tags): list of physical phenomena                         |
| `homepage`          | Yes      | An URL to the homepage                                              |
| `institutions`      | No       | A list of institutions (full names)                                 |
| `institution_link`  | No       | A list of urls to the institutions                                  |
| `repository`        | No       | An URL to the primary source code repository                        |
| `issue_tracker`     | No       | An URL to the primary issue tracker                                 |
| `platform`          | No       | List for: `linux`, `macos`, `windows`                                 |
| `license`           | Yes      | The [SPDX license identifier](https://spdx.org/licenses/) or "freeware", "proprietary", "collaborators/MoU", or "unknown", as appropriate |
| `publication`       | No       | The preferred citation by the code authors                          |
| `publication_link`  | No       | An URL, ideally a `https://doi.org/<DOI>`, to the publication above |

The file `schema.json` ([JSON schema](https://json-schema.org/) is used to programatically check the schema once entries are changed.

## Process the Database

### Python

The `codes.json` file is our central database for all information.
If you like to process and filter this list for your purpose, you could for instance load the whole list with Python:

```py
import json

# Local file
codes = json.load(open("codes.json"))["codes"]

# Remote file 
import urllib.request
URL  = "https://campa-consortium.github.io/accelerator_simulation_codes/codes.json"
with urllib.request.urlopen(URL) as url:
    codes = json.loads(url.read().decode())['codes']


type(codes)
# list: each code is one entry

type(codes[0])
# dict: a code entry with keywords as defined above

len(codes)
# 55 as of January 2022
```

### Web Endpoints

If you like to dynamically load the `codes.json` file into (web) applications, you can query the latest version from this endpoint:
https://campa-consortium.github.io/accelerator_simulation_codes/codes.json
