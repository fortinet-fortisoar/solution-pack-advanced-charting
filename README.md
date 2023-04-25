# Release Information

* **Version**: 1.0.0
* **Certified**: No
* **Publisher**: Fortinet
* **Compatible Version**: 7.3.1

# Overview

The Time Series Charts Solution Pack helps generate data-over-time charts for Dashboards and Reports, allowing for more effective trend reporting and pattern illustration.

The solution pack installs a widget, a connector, a new module, and a playbook collection to deliver the data-over-time charting capability. Additionally, an included sample Dashboard acts as a reference when building your Time Series Charts with the included components.

# Overall Design

Although the Solution Pack includes multiple components, the user's primary interaction is with the included widget. Creating and Configuring this widget creates and updates modules in the included Time Series Charts module. These actions in the Module then trigger the included playbooks that perform the necessary queries and store the results in the module record. Finally, when the user opens a report or dashboard containing the widget instance, the widget pulls the query results from the module record and renders them as a chart.

# Next Steps

| [Installation](./docs/setup.md#installation) | [Configuration](./docs/setup.md#configuration) | [Usage](./docs/usage.md) | [Contents](./docs/contents.md) |
|----------------------------------------------|------------------------------------------------|--------------------------|--------------------------------|
