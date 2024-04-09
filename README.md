<p align="center">
   <img src="logo.jpg" width="300" alt="Home Assistant Add-on VictoriaLogs Database for logs">
</p>

# Home Assistant Add-on VictoriaLogs Database for logs

[VictoriaLogs](https://docs.victoriametrics.com/victorialogs/) is [open source](https://github.com/VictoriaMetrics/VictoriaMetrics/tree/master/app/victoria-logs) user-friendly database for logs from [VictoriaMetrics](https://github.com/VictoriaMetrics/VictoriaMetrics/).

This add-on makes it easy to run a VictoriaLogs on Home Assistant OS on ARM64 systems like Raspberry Pi 4 or AMD64.

## VictoriaLogs provides the following key features:
  
- [VictoriaLogs](https://docs.victoriametrics.com/victorialogs/) can accept logs from popular log collectors. See [these docs](https://docs.victoriametrics.com/victorialogs/data-ingestion/).
- [VictoriaLogs](https://docs.victoriametrics.com/victorialogs/) is much easier to set up and operate compared to Elasticsearch and Grafana Loki. See [these docs](https://docs.victoriametrics.com/victorialogs/quickstart/).
-   [VictoriaLogs](https://docs.victoriametrics.com/victorialogs/) provides easy yet powerful query language with full-text search capabilities across all the [log fields](https://docs.victoriametrics.com/victorialogs/keyconcepts/#data-model) - see [LogsQL docs](https://docs.victoriametrics.com/victorialogs/logsql/).
- [VictoriaLogs](https://docs.victoriametrics.com/victorialogs/) can be seamlessly combined with good old Unix tools for log analysis such as `grep`, `less`, `sort`, `jq`, etc. See [these docs](https://docs.victoriametrics.com/victorialogs/querying/#command-line) for details.
- [VictoriaLogs](https://docs.victoriametrics.com/victorialogs/) capacity and performance scales linearly with the available resources (CPU, RAM, disk IO, disk space). It runs smoothly on both Raspberry PI and a server with hundreds of CPU cores and terabytes of RAM.
- [VictoriaLogs](https://docs.victoriametrics.com/victorialogs/) can handle up to 30x bigger data volumes than Elasticsearch and Grafana Loki when running on the same hardware. See [these docs](https://docs.victoriametrics.com/victorialogs/#benchmarks).
- [VictoriaLogs](https://docs.victoriametrics.com/victorialogs/) supports fast full-text search over high-cardinality [log fields](https://docs.victoriametrics.com/victorialogs/keyconcepts/#data-model) such as `trace_id`, `user_id` and `ip`.
- [VictoriaLogs](https://docs.victoriametrics.com/victorialogs/) supports multitenancy - see [these docs](https://docs.victoriametrics.com/victorialogs/#multitenancy).
- [VictoriaLogs](https://docs.victoriametrics.com/victorialogs/) supports out-of-order logs’ ingestion aka backfilling.
- [VictoriaLogs](https://docs.victoriametrics.com/victorialogs/) provides a simple web UI for querying logs - see [these docs](https://docs.victoriametrics.com/victorialogs/querying/#web-ui).

[VictoriaLogs on GitHub](https://github.com/VictoriaMetrics/VictoriaMetrics)


## Installation and configuration

1. Add the reposity. (Quick link: [![Open your Home Assistant instance and show the Supervisor add-on store.](https://my.home-assistant.io/badges/supervisor_store.svg)](https://my.home-assistant.io/redirect/supervisor_store/) )
    * **Add the reposity** (click 3 dots on the top right of the screen). Reposity URL: *https://github.com/denisgolius/homeassistant-addon-victorialogs*
    * Refresh/reload your browser tab/window

2. **Install** the add-on:
    * Find, and **install** the VictoriaLogs add-on

3. Configure VictoriaLogs
   > Read the [addon documentation](victoria-logs/DOCS.md) which can also be found on the **Documentation tab** of the [VictoriaLogs addon](https://my.home-assistant.io/redirect/supervisor_store/) in the Home Assistant settings. Check also a [list of supported command-line flags](https://docs.victoriametrics.com/victorialogs/#list-of-command-line-flags) with their description.

4. **Start** the *VictoriaLogs* add-on

    > Don't forget to restart Home Assistant!


Well done! You can install and configure Grafana or similar to check data is being logged.
