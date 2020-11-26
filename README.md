# LGBTIQ-Report-Data

This repo contains supporting data for the report REPORT-TITLE-HERE released jointly by [Citizen Lab](https://citizenlab.ca/), [OONI](https://ooni.org/) and [Outright International](https://outrightinternational.org/).

# Data

Throughout the data, there is reference to annotations, these are documented text patterns that indicate
a possible blocking behaviour.  These names are documented here:

* [DNS](https://github.com/citizenlab/filtering-annotations/blob/master/data/v1/dns.csv) for DNS reply based annotations
* [HTTP](https://github.com/citizenlab/filtering-annotations/blob/master/data/v1/http.csv) for HTTP(S) reply based annotations

## Top Level Directory

The top level directory contains the [testlist](testlist.txt) that was used in the study. 

It also contains CSV files of all blocked results in the countries:

Schema:

* **url** - The URL that was tested
* **times_tested_total** - The number of times the URL was tested in the course of the study.
* **times_seen_any_ann** - The number of times any annotation (DNS or HTTP) was seen for the URL
* **annotation_pct** - The percentage of measurements that have any annotations.
* **time_seen_dns_ann** - The number of times any DNS based signature matches.
* **times_seen_http_ann** - The number of times any HTTP based signature matches.
* **first_time_an_annotation_seen** - The first date where any annotation is seen for the URL.
* **last_time_an_annotation_seen** - The most recent date where any annotation is seen for the URL.
* **block_duration_days** - The number of days a block was present. As testing is opportunistic this refers to the number of days between first_time and last_time values.
* **num_uniq_annotations** - The number of unique annotations that match for the URL.
* **num_asns_seen** - The number of distinct AS Numbers that see a single annotation.
* **ann_list** - All annotation names that match for the given tested URL.
* **num_asns_seen** - The number of distinct AS Numbers that see a single annotation.
* **asn_name_list** - All AS name values where an annotation is seen.
* **asn_num_list** - All AS num values where an annotation is seen.

## annotations_stats

This directory includes per country annotation statistics.  It is a full table of annotation name and the number of unique URLs where an annotation was seen.

## asn_stats

This directory includes per country ASN statistics.  It is a full table of AS numbers and the number of unique URLs where an annotation was seen.

## id-events

This contains the excluded results for Indonesia based on the two blocking events: MNC event and Telkom event as documented in the methodology section of the report

## testing_coverage

This directory contains all networks where testing was done (not just those where annotations were present)  This is used to get a sense of how 
widely a given country was tested and where those URLs were tested.  The count figure in these csv files refers to the unique measurements that were in tested.

## unfiltered

This contains all results with annotations in the country without excluding any results and prior to merging as described in the methodology section of the report.

# License

All supporting data is provided under Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International and available in full
[here](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode) and summarized
[here](https://creativecommons.org/licenses/by-nc-sa/4.0/)