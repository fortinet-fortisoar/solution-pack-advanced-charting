# Release Information

* **Version**: 1.0.0
* **Certified**: No
* **Publisher**: Fortinet
* **Compatible Version**: 7.3.1

# Overview

The Time Series Charts Solution Pack adds the capability to generate data-over-time charts for use  on Dashboards and Reports, allowing for more effective trend reporting and pattern illustration.

The Solution Pack installs a Widget, a Connector a new Module, as well as a Playbook collection which function together to deliver the charting capability mentioned above. Additionally, a sample Dashboard is included to use as a reference when building your own Time Series Charts with the included components.

# Overall Design

Although the Solution Pack includes multiple components, the User's interaction with the Solution Pack will be primarily with the included Widget. Creating and Configuring instances of the Widget will cause records to be created and updated in the included Time Series Charts Module. These actions in the Module then trigger the included Playbooks, which perform the necessary queries and store the results in the Module record. Finally, when the user opens a Report or Dashboard which contains the Widget instance, the Widget will pull the query results from the Module record and render them as a chart.

# Next Steps

| [Installation](./docs/setup.md#installation) | [Configuration](./docs/setup.md#configuration) | [Usage](./docs/usage.md) | [Contents](./docs/contents.md) |
|--------------------------------------------|----------------------------------------------|------------------------|------------------------------|
