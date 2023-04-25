| [Home](../README.md) |
|--------------------------------------------|

# Installation

1. To install a solution pack, click **Content Hub** > **Discover**.
2. From the list of solution pack that appears, search for and select `Time Series Charts`.
3. Click the `Time Series Charts` solution pack card.
4. Click **Install** on the bottom to begin the installation.

## Prerequisites

This solutions pack has no prerequisites.

# Configuration

## Configuring Permissions for the Time Series Charts Module
The Time Series Charts Solution Pack includes a Module called "Time Series Charts" which will store chart configuration information as well as query results. After installing this solution pack, permissions will need to be set up for this Module. At a minimum, the Playbook Appliance must be set to a role that has full Read, Update, and Delete permissions on the Time Series Charts Module. In addition, Users who will be viewing the resulting charts will require Read permissions, and those who will be creating and configuring them will require Create and Update permissions.

## Configuring the Time Series Charts Widget
Provide the following details to customize the Time Series Charts Widget to suit your requirements:

| Fields     | Description                              |
| ---------- | ---------------------------------------- |
| Title      | Provide the text which will appear above the rendered chart. |
| Time Axis View (X) | The length of the "buckets" into which the events on the rendered chart will be grouped (for example Hourly, Daily, etc.) and the period which the chart will cover (for example "in the last 7 days", "in the last  3 months", etc.) |

For each Data Set (whether individual or as a part of a Data Set Group), the following additional details may be customized:

| Fields     | Description                              |
| ---------- | ---------------------------------------- |
| Data Set Title      | This is the label that will be associated with this Data Set on the rendered chart |
| Data Source | The module which will be queried for this Data Set |
| Plot Type | How this Data Set will be represented on the resulting chart. For example Bar, Line, Scatter, etc. |
| Field to Build Time Axis With | The field in the corresponding module which will dictate each record's place on the chart's X-Axis |
| Group Results By (optional, individual Data Sets only) | Setting this parameter will automatically break the results of this Data Set's query up into separate representations (bars, scatter point groups, etc) for each value in the picklist field chosen. For example, setting this to "Severity" will result in separate representations for "High", "Medium", and "Low" in the resulting chart. |
| Filter Criteria | Set the filters which will determine which records from the chosen module are represented in this Data Set |

## Scheduling Chart Updates and Cleanup

The included Playbook Collection contains a Playbook which will update existing charts with up-to-date data. This Playbook will need to be scheduled to keep adding data to configured Time Series Charts. This can be done by performing the following steps:

1. On the left navigation pane, select **Schedules**.
2. Select **Create New Schedule**.
3. In the *Schedule modal* which appears, give an appropriate name to your schedule and set the frequency to update as you see fit.
4. In the **Playbook Reference** field, select the **Update All Time Series Charts** playbook.
5. Ensure that the **Start Schedule** checkbox is selected.
6. Save the schedule.

## Scheduling Unused Record Cleanup

As Dashboards and Reports are modified, some instances of the Time Series Chart Widget may be deleted. The included Playbook Collection includes a playbook that will find and delete any Time Series Chart module records that no longer correspond to an active instance of the Time Series Charts Widget. It is recommended to set this playbook to run periodically on a schedule, using the following steps:

1. On the left navigation pane, select **Schedules**.
2. Select **Create New Schedule**.
3. In the *Schedule modal* which appears, give an appropriate name to your schedule and set the frequency to update as you see fit. This playbook does not need to run often, so a weekly or less frequent schedule will be sufficient.
4. In the **Playbook Reference** field, select the **Clean Up Unused Chart Records** playbook.
5. Ensure that the "Start Schedule" checkbox is selected.
6. Save the schedule.

| [Usage](./docs/usage.md) | [Contents](./docs/contents.md) |
|--------------------------|--------------------------------|