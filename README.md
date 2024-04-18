<div align="center">
	<br>
	<img src="header.svg" width="100%" height="100%" alt="Test">
	<br>
</div>

<div width="100%">
<table><tbody>
                <tr>
                    <th width="20%">Type:</th>
                    <td width="100%"><code>scope</code></td>
                </tr>
                <tr>
                    <th width="20%">Root object:</th>
                    <td width="100%">PcpInputParams</td>
                </tr>
                <tr>
                    <th width="20%">Properties</th>
                    <td width="100%"><details><summary>flatten (<code>bool</code>)</summary>
                        <table><tbody>
                            <tr>
                                <th>Name:</th>
                                <td>flatten JSON structure</td>
                            </tr>
                            <tr>
                                <th>Description:</th>
                                <td>Processes the metrics first into a two-dimensional format via the pcp2csv converter, and then converts the CSV to JSON, effectively flattening the data structure. This is useful when indexing metrics to a service like Elasticsearch.</td>
                            </tr>
                        </tbody></table>
                    </details></td>
                </tr>
                </tbody></table>
</div>

<!-- Autogenerated documentation by arcaflow-docsgen
## Start PCP (`start-pcp`)

Start the PCP data logging tools

### Input

<table><tbody>
<tr><th>Type:</th><td><code style="white-space: nowrap">scope</code></td><tr><th>Root object:</th><td>PcpInputParams</td></tr>
<tr><th>Properties</th><td><details><summary>flatten (<code style="white-space: nowrap">bool</code>)</summary>
                <table><tbody><tr><th>Name:</th><td>flatten JSON structure</td></tr><tr><th>Description:</th><td>Processes the metrics first into a two-dimensional format via the pcp2csv converter, and then converts the CSV to JSON, effectively flattening the data structure. This is useful when indexing metrics to a service like Elasticsearch.</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Default (JSON encoded):</th><td><pre><code style="white-space: nowrap">false</code></pre></td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">bool</code></td></tbody></table>
            </details><details><summary>generate_csv (<code style="white-space: nowrap">bool</code>)</summary>
                <table><tbody><tr><th>Name:</th><td>generate CSV output</td></tr><tr><th>Description:</th><td>Generates the data payload also in CSV format. This output goes to the debug_logs, or to stderr if the --debug flag is used.</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Default (JSON encoded):</th><td><pre><code style="white-space: nowrap">false</code></pre></td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">bool</code></td></tbody></table>
            </details><details><summary>pmlogger_conf (<code style="white-space: nowrap">string</code>)</summary>
                <table><tbody><tr><th>Name:</th><td>pmlogger configuration file</td></tr><tr><th>Description:</th><td>Complete configuration file content for pmlogger as a multi-line string. If no config file is provided, a default one will be generated. NOTE: Input not validated by the plugin -- Any errors are likely to be produced at the end of the plugin run and may result in workflow failures.</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">string</code></td></tbody></table>
            </details><details><summary>pmlogger_interval (<code style="white-space: nowrap">float</code>)</summary>
                <table><tbody><tr><th>Name:</th><td>pmlogger logging interval</td></tr><tr><th>Description:</th><td>The logging interval in seconds (float) used by pmlogger for data collection</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Default (JSON encoded):</th><td><pre><code style="white-space: nowrap">1.0</code></pre></td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">float</code></td><tr><th>Units:</th><td>nanoseconds</td></tr>
</tbody></table>
            </details><details><summary>pmlogger_metrics (<code style="white-space: nowrap">string</code>)</summary>
                <table><tbody><tr><th>Name:</th><td>pmlogger metrics to report</td></tr><tr><th>Description:</th><td>The pmrep-compatible metrics values to report as a space-separated string. NOTE: Input not validated by the plugin -- Any errors are likely to be produced at the end of the plugin run and may result in workflow failures.</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Default (JSON encoded):</th><td><pre><code style="white-space: nowrap">&#34;:vmstat :sar :sar-B :sar-w :sar-b :sar-H :sar-r&#34;</code></pre></td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">string</code></td></tbody></table>
            </details><details><summary>pmrep_conf (<code style="white-space: nowrap">string</code>)</summary>
                <table><tbody><tr><th>Name:</th><td>pmrep configuration file</td></tr><tr><th>Description:</th><td>Complete configuration file content for pmrep as a multi-line string. If no config file is provided, a default one will be used. This configuration is used internally for `pcp2json` and `pcp2csv`. NOTE: Input not validated by the plugin -- Any errors are likely to be produced at the end of the plugin run and may result in workflow failures.</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">string</code></td></tbody></table>
            </details><details><summary>timeout (<code style="white-space: nowrap">int</code>)</summary>
                <table><tbody><tr><th>Name:</th><td>pmlogger timeout seconds</td></tr><tr><th>Description:</th><td>Timeout in seconds after which to cancel the pmlogger collection</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">int</code></td>
</tbody></table>
            </details></td></tr>
<tr><td colspan="2"><details><summary><strong>Objects</strong></summary><details><summary>PcpInputParams (<code style="white-space: nowrap">object</code>)</summary>
            <table><tbody><tr><th>Type:</th><td><code style="white-space: nowrap">object</code></td><tr><th>Properties</th><td><details><summary>flatten (<code style="white-space: nowrap">bool</code>)</summary>
        <table style="width:100%"><tbody><tr><th>Name:</th><td>flatten JSON structure</td></tr><tr><th>Description:</th><td>Processes the metrics first into a two-dimensional format via the pcp2csv converter, and then converts the CSV to JSON, effectively flattening the data structure. This is useful when indexing metrics to a service like Elasticsearch.</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Default (JSON encoded):</th><td><pre><code style="white-space: nowrap">false</code></pre></td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">bool</code></td></tbody></table>
        </details><details><summary>generate_csv (<code style="white-space: nowrap">bool</code>)</summary>
        <table style="width:100%"><tbody><tr><th>Name:</th><td>generate CSV output</td></tr><tr><th>Description:</th><td>Generates the data payload also in CSV format. This output goes to the debug_logs, or to stderr if the --debug flag is used.</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Default (JSON encoded):</th><td><pre><code style="white-space: nowrap">false</code></pre></td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">bool</code></td></tbody></table>
        </details><details><summary>pmlogger_conf (<code style="white-space: nowrap">string</code>)</summary>
        <table style="width:100%"><tbody><tr><th>Name:</th><td>pmlogger configuration file</td></tr><tr><th>Description:</th><td>Complete configuration file content for pmlogger as a multi-line string. If no config file is provided, a default one will be generated. NOTE: Input not validated by the plugin -- Any errors are likely to be produced at the end of the plugin run and may result in workflow failures.</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">string</code></td></tbody></table>
        </details><details><summary>pmlogger_interval (<code style="white-space: nowrap">float</code>)</summary>
        <table style="width:100%"><tbody><tr><th>Name:</th><td>pmlogger logging interval</td></tr><tr><th>Description:</th><td>The logging interval in seconds (float) used by pmlogger for data collection</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Default (JSON encoded):</th><td><pre><code style="white-space: nowrap">1.0</code></pre></td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">float</code></td><tr><th>Units:</th><td>nanoseconds</td></tr>
</tbody></table>
        </details><details><summary>pmlogger_metrics (<code style="white-space: nowrap">string</code>)</summary>
        <table style="width:100%"><tbody><tr><th>Name:</th><td>pmlogger metrics to report</td></tr><tr><th>Description:</th><td>The pmrep-compatible metrics values to report as a space-separated string. NOTE: Input not validated by the plugin -- Any errors are likely to be produced at the end of the plugin run and may result in workflow failures.</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Default (JSON encoded):</th><td><pre><code style="white-space: nowrap">&#34;:vmstat :sar :sar-B :sar-w :sar-b :sar-H :sar-r&#34;</code></pre></td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">string</code></td></tbody></table>
        </details><details><summary>pmrep_conf (<code style="white-space: nowrap">string</code>)</summary>
        <table style="width:100%"><tbody><tr><th>Name:</th><td>pmrep configuration file</td></tr><tr><th>Description:</th><td>Complete configuration file content for pmrep as a multi-line string. If no config file is provided, a default one will be used. This configuration is used internally for `pcp2json` and `pcp2csv`. NOTE: Input not validated by the plugin -- Any errors are likely to be produced at the end of the plugin run and may result in workflow failures.</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">string</code></td></tbody></table>
        </details><details><summary>timeout (<code style="white-space: nowrap">int</code>)</summary>
        <table style="width:100%"><tbody><tr><th>Name:</th><td>pmlogger timeout seconds</td></tr><tr><th>Description:</th><td>Timeout in seconds after which to cancel the pmlogger collection</td></tr><tr><th>Required:</th><td>No</td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">int</code></td>
</tbody></table>
        </details></td></tr>
</tbody></table>
        </details></details></td></tr>
</tbody></table>

### Outputs


#### error

<table><tbody>
<tr><th>Type:</th><td><code style="white-space: nowrap">scope</code></td><tr><th>Root object:</th><td>Error</td></tr>
<tr><th>Properties</th><td><details><summary>error (<code style="white-space: nowrap">string</code>)</summary>
                <table><tbody><tr><th>Required:</th><td>Yes</td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">string</code></td></tbody></table>
            </details></td></tr>
<tr><td colspan="2"><details><summary><strong>Objects</strong></summary><details><summary>Error (<code style="white-space: nowrap">object</code>)</summary>
            <table><tbody><tr><th>Type:</th><td><code style="white-space: nowrap">object</code></td><tr><th>Properties</th><td><details><summary>error (<code style="white-space: nowrap">string</code>)</summary>
        <table style="width:100%"><tbody><tr><th>Required:</th><td>Yes</td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">string</code></td></tbody></table>
        </details></td></tr>
</tbody></table>
        </details></details></td></tr>
</tbody></table>

#### success

<table><tbody>
<tr><th>Type:</th><td><code style="white-space: nowrap">scope</code></td><tr><th>Root object:</th><td>PerfOutput</td></tr>
<tr><th>Properties</th><td><details><summary>pcp_output (<code style="white-space: nowrap">list[<code style="white-space: nowrap">
    any</code>]</code>)</summary>
                <table><tbody><tr><th>Name:</th><td>PCP output list</td></tr><tr><th>Description:</th><td>List of of performance data in intervals from PCP</td></tr><tr><th>Required:</th><td>Yes</td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">list[<code style="white-space: nowrap">
    any</code>]</code></td><tr><td colspan="2">
    <details>
        <summary>List items</summary>
        <table><tbody><tr><th>Type:</th><td><code style="white-space: nowrap">
    any</code></td></tbody></table>
    </details>
</td></tr></tbody></table>
            </details></td></tr>
<tr><td colspan="2"><details><summary><strong>Objects</strong></summary><details><summary>PerfOutput (<code style="white-space: nowrap">object</code>)</summary>
            <table><tbody><tr><th>Type:</th><td><code style="white-space: nowrap">object</code></td><tr><th>Properties</th><td><details><summary>pcp_output (<code style="white-space: nowrap">list[<code style="white-space: nowrap">
    any</code>]</code>)</summary>
        <table style="width:100%"><tbody><tr><th>Name:</th><td>PCP output list</td></tr><tr><th>Description:</th><td>List of of performance data in intervals from PCP</td></tr><tr><th>Required:</th><td>Yes</td></tr><tr><th>Type:</th><td><code style="white-space: nowrap">list[<code style="white-space: nowrap">
    any</code>]</code></td><tr><td colspan="2">
    <details>
        <summary>List items</summary>
        <table><tbody><tr><th>Type:</th><td><code style="white-space: nowrap">
    any</code></td></tbody></table>
    </details>
</td></tr></tbody></table>
        </details></td></tr>
</tbody></table>
        </details></details></td></tr>
</tbody></table>
 End of autogenerated documentation -->