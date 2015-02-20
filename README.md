# Munin plugins

Some custom [Munin](http://munin-monitoring.org/) plugins to use
on FreeBSD.

* ```zfsarc``` - monitors ZFS ARC usage as reported by FreeBSD
top(1). Reports total memory used my ARC as well as breakdown to
MFU, MRU, Anon, Header and Other sizes.
* ```poudriere_``` - monitors poudriere port build status for
selected build. Shows number of totally queued ports and breakdown
to built/failed/skipped/ignored/remaining ports. Only reports data
when the build is in progress.
