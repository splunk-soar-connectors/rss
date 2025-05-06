# RSS

Publisher: Splunk \
Connector Version: 2.2.3 \
Product Vendor: Generic \
Product Name: RSS \
Minimum Product Version: 6.1.1

Ingest IOCs from an RSS Feed

## Modules

This app uses the sgmllib3k module which is licensed under the BSD 2-Clause license

### Configuration variables

This table lists the configuration variables required to operate RSS. These variables are specified when configuring a RSS asset in Splunk SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**rss_feed** | required | string | RSS Feed |
**save_file** | optional | boolean | Save file to vault |
**container_count** | optional | numeric | Maximum entries to parse (0 for all) |
**artifact_count** | optional | numeric | Maximum artifacts to create per entry (0 for all) |
**ignore_perrors** | optional | boolean | Ignore parsing errors |
**ignore_cterrors** | optional | boolean | Ignore content type errors |

### Supported Actions

[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration \
[on poll](#action-on-poll) - Ingest IOCs from an RSS Feed

## action: 'test connectivity'

Validate the asset configuration for connectivity using supplied configuration

Type: **test** \
Read only: **True**

#### Action Parameters

No parameters are required for this action

#### Action Output

No Output

## action: 'on poll'

Ingest IOCs from an RSS Feed

Type: **ingest** \
Read only: **True**

The action ingests RSS feeds where entries point to HTML or PDF documents only.

#### Action Parameters

PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**container_count** | optional | Maximum number of events to query for | numeric | |
**artifact_count** | optional | Maximum number of artifacts per container | numeric | |
**start_time** | optional | Parameter is ignored in this app | string | |
**end_time** | optional | Parameter is ignored in this app | string | |

#### Action Output

No Output

______________________________________________________________________

Auto-generated Splunk SOAR Connector documentation.

Copyright 2025 Splunk Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and limitations under the License.
