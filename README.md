# DESCRIPTION #

Configure plugins for the [collectd](http://collectd.org/) monitoring daemon.

# REQUIREMENTS #

This cookbook has only been tested on Ubuntu 10.04.

# USAGE #

A number of recipes for standard plugins are available:

* `collectd_plugins::rrdtool` - Output to RRD database files.
* `collectd_plugins::syslog` Log errors to syslog.
* `collectd_plugins::cpu` - CPU usage.
* `collectd_plugins::df` - Free space on disks.
* `collectd_plugins::disk` - Disk I/O operations.
* `collectd_plugins::interface` - Network I/O operations.
* `collectd_plugins::memory` - Memory usage.
* `collectd_plugins::swap` - Swap file usage.
* `collectd_plugins::write_graphite` - Stores values in Carbon, the storage layer of Graphite.

It is recommended to always enable the first two (rrdtool and syslog), but the others are entirely optional. For convenience, the `collectd_plugins` default recipe will include all of these (except `write_graphite`).

## Redis ##

A plugin to monitor [Redis](http://redis.io/) is included as `collectd_plugins::redis`. This recipe requires that you be using our [redis cookbook](https://github.com/AtariTech/cookbooks/tree/master/redis)
for your servers, but can be trivially modified to look for a different recipe or role name.

# LICENSE & AUTHOR #

Author:: Noah Kantrowitz (<noah@coderanger.net>)
Copyright:: 2010, Atari, Inc

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
