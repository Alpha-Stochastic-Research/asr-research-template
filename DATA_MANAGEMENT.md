# Data Management Plan

## Data Summary

Describe the datasets used or produced by this project.

Include:

* Dataset name
* Data provider
* Data format
* Estimated size
* Time period covered
* Update frequency

## Data Sources

| Dataset | Source | Access Method | License | Status  |
| ------- | ------ | ------------- | ------- | ------- |
|         |        |               |         | Planned |

## Data Classification

Select the appropriate classification:

* [ ] Public
* [ ] Internal
* [ ] Confidential
* [ ] Restricted

Do not commit confidential or restricted data to the repository.

## Data Provenance

For each dataset, document:

* Where the data originated
* When it was collected or downloaded
* Who collected it
* Any transformations applied
* The original file name or identifier
* The version or retrieval date

## Licensing and Usage Rights

Document:

* The dataset license
* Redistribution permissions
* Commercial-use restrictions
* Attribution requirements
* Any contractual restrictions

Do not publish data unless redistribution is explicitly permitted.

## Storage

Describe where each type of data is stored.

| Data Type          | Storage Location                      | Included in Git | Backup |
| ------------------ | ------------------------------------- | --------------: | -----: |
| Public sample data | `data/sample/`                        |             Yes |    Yes |
| Raw data           | External storage                      |              No |    Yes |
| Processed data     | External storage or generated locally |              No |    Yes |
| Confidential data  | Approved secure storage               |              No |    Yes |

## Repository Rules

The following files must not be committed:

* API keys
* Passwords
* Authentication tokens
* `.env` files
* Private keys
* Confidential datasets
* Personal data
* Licensed market data without redistribution rights
* Unpublished restricted research material

## Data Structure

Recommended structure:

```text
data/
├── README.md
├── sample/
├── raw/
├── interim/
├── processed/
└── external/
```

Only public, redistributable sample data should normally be committed.

## Data Processing

Document the complete processing pipeline:

```text
Raw data
→ validation
→ cleaning
→ transformation
→ analysis dataset
→ results
```

Processing scripts should be reproducible and stored in the repository.

## Data Quality

Document checks for:

* Missing values
* Duplicate records
* Invalid values
* Outliers
* Date consistency
* Unit consistency
* Currency consistency
* Survivorship bias
* Look-ahead bias
* Data leakage

## Personal and Sensitive Data

If the project uses personal or sensitive information:

* Document the lawful basis for processing.
* Minimize the collected information.
* Remove direct identifiers when possible.
* Restrict access to authorized people.
* Define a retention and deletion policy.
* Do not include the data in public repositories.

## Retention and Deletion

Describe:

* How long the data will be retained
* Who is responsible for deletion
* Which backups must also be deleted
* Whether processed results may be retained

## Reproducibility

Another researcher should be able to understand:

* Which data is required
* Where it can legally be obtained
* How it is prepared
* Which scripts process it
* Which version was used
* Why any data cannot be shared

## Approval Checklist

* [ ] Data sources are documented.
* [ ] Data licenses have been reviewed.
* [ ] Sensitive data is identified.
* [ ] Restricted data is excluded from Git.
* [ ] Data-processing steps are reproducible.
* [ ] Data-quality checks are documented.
* [ ] Retention and deletion requirements are defined.
* [ ] The plan has been reviewed by `release-admins`.
