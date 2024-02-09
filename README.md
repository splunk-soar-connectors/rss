[comment]: # "Auto-generated SOAR connector documentation"
# RSS

Publisher: Splunk  
Connector Version: 2.2.2  
Product Vendor: Generic  
Product Name: RSS  
Product Version Supported (regex): ".\*"  
Minimum Product Version: 6.1.1  

Ingest IOCs from an RSS Feed

[comment]: # " File: README.md"
[comment]: # "  Copyright (c) 2017-2022 Splunk Inc."
[comment]: # ""
[comment]: # "  Licensed under Apache 2.0 (https://www.apache.org/licenses/LICENSE-2.0.txt)"
[comment]: # ""
## Modules

This app uses the sgmllib3k module which is licensed under the BSD 2-Clause license


### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a RSS asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**rss_feed** |  required  | string | RSS Feed
**save_file** |  optional  | boolean | Save file to vault
**container_count** |  optional  | numeric | Maximum entries to parse (0 for all)
**artifact_count** |  optional  | numeric | Maximum artifacts to create per entry (0 for all)
**ignore_perrors** |  optional  | boolean | Ignore parsing errors
**ignore_cterrors** |  optional  | boolean | Ignore content type errors

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[on poll](#action-on-poll) - Ingest IOCs from an RSS Feed  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'on poll'
Ingest IOCs from an RSS Feed

Type: **ingest**  
Read only: **True**

The action ingests RSS feeds where entries point to HTML or PDF documents only.

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**container_count** |  optional  | Maximum number of events to query for | numeric | 
**artifact_count** |  optional  | Maximum number of artifacts per container | numeric | 
**start_time** |  optional  | Parameter is ignored in this app | string | 
**end_time** |  optional  | Parameter is ignored in this app | string | 

#### Action Output
No Output