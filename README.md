# Nibbler

Yet another collector for Mesos. Aiming to be as robust and platform (Mesos version) independent as possible.

## Dependencies

 - InfluxDB 0.8.X
 - Python 2.8.X (`requests` library)

## Usage

```bash
usage: slave-collect.py [-h] [--slave SLAVE] [--influxdb-host INFLUXDB_HOST]
                        --influxdb-name INFLUXDB_NAME
                        [--influxdb-user INFLUXDB_USER]
                        [--influxdb-password INFLUXDB_PASSWORD]
```

<table>
<thead>
<th>Flag</th>
<th>Description</th>
</thead>
<tr>
<td>slave</td>
<td>hostname and port for mesos slave</td>
</tr>
<tr>
<td>influxdb-name</td>
<td>hostname and port for influxdb admin server (default: localhost:8086)</td>
</tr>
<tr>
<td>influxdb-name</td>
<td>database name to use</td>
</tr>
<tr>
<td>influxdb-user</td>
<td>user for influxdb admin server</td>
</tr>
<tr>
<td>influxdb-password</td>
<td>password for influxdb admin server</td>
</tr>
</table>

Example:

```bash
$ python slave-collect.py --influxdb-name=mesos --slave=localhost:5050
<Response [200]>
Sent sample...
<Response [200]>
Sent sample...
<Response [200]>
Sent sample...
```
