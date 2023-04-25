| [Home](../README.md) |
|--------------------------------------------|

# Contents

The `**Solution Pack's Name**` solution pack contains the following resources.

## Connectors

|**Name**|**Description**|
| :- | :- |
| Time Series Chart Utilities | Provides useful processing functions to process and submit queries needed for Time Series Charts |

## Module Schema

|**Name**|**Description**|
| :- | :- |
| Time Series Charts | Contains the configuration data for a Time Series Chart Widget instance, plus the results of  the corresponding queries |

## Playbook Collection

| 10 - SP - Time Series Charts |
| :- | :- |


**Playbook Name**|**Description**|
| :- | :- |
| Clean Up Unused Chart Records | Searches for records in the Time Series Charts module which do not correspond to active instances of the Time Series Charts Widget and deletes them |
| Manually Run Chart Queries and Update Record | Allows users to trigger the update process for a specific chart from the Time Series Charts Module |
| Time Series Chart - Trigger Chart Queries (Upon Creation) | Triggers the initial chart update process whenever a record is created in the Time Series Charts Module. This usually happens when a new instance of the Time Series Charts Widget is configured |
| Time Series Chart - Trigger Chart Queries (When Updated) | Triggers the chart update process whenever a record in the Time Series Charts Module is modified and its 'Chart Config Updated' field is set to True. This usually will happen whenever the configuration for an instance of the Time Series Charts Widget is modified |
| > Prepare for Chart Queries | Pulls the chart configuration from a single record in the Time Series Charts Module and builds the base queries for it. This playbook then calls the ">> Run Chart Query On Time Buckets" playbook before adding the query results to the Time Series Charts record |
| >> Run Chart Queries on Time Buckets | Takes the base query for a single Data Set, as well as the list of time windows which need to be queried and performs the base query bounded by each of those time windows. Outputs the results of these queries |
| Update All Time Series Charts | Calls the "> Prepare for Chart Queries" playbook for all records in the Time Series Charts Module. This effectively updates the data in all Time Series Chart Widgets. This playbook should be run on a schedule to keep the charts up-to-date |

>**Warning:** We recommend that you clone these playbooks before customizing to avoid loss of information while upgrading the solution pack.

| [Installation](./docs/setup.md#installation) | [Configuration](./docs/setup.md#configuration) | [Usage](./docs/usage.md) |
|----------------------------------------------|------------------------------------------------|--------------------------|