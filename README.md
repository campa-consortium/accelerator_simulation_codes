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
| `institution_link`  | No       | An URL to the primary institution / project head                    |
| `repository`        | No       | An URL to the primary source code repository                        |
| `issue_tracker`     | No       | An URL to the primary issue tracker                                 |
| `license`           | Yes      | The [SPDX license identifier](https://spdx.org/licenses/) or "freeware", "proprietary", "collaborators/MoU", or "unknown", as appropriate |
| `publication`       | No       | The preferred citation by the code authors                          |
| `publication_link`  | No       | An URL, ideally a `https://doi.org/<DOI>`, to the publication above |

The file `schema.json` ([JSON schema](https://json-schema.org/) is used to programatically check the schema once entries are changed.
