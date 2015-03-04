# Munin plugins

Some custom [Munin](http://munin-monitoring.org/) plugins to use
on FreeBSD.

## Original plugins

* ```zfsarc``` - monitors ZFS ARC usage as reported by FreeBSD
top(1). Reports total memory used my ARC as well as breakdown to
MFU, MRU, Anon, Header and Other sizes.
* ```poudriere_``` - monitors poudriere port build status for
selected build. Shows number of totally queued ports and breakdown
to built/failed/skipped/ignored/remaining ports. Only reports data
when the build is in progress.
* ```bruteblock``` - monitors size of ipfw table which contains
hosts blocked by bruteblock

## Modifications of standard plugins

* ```df```
  * Calculate accurate filesystem usage percent instead of using rounded one
  * Ignore tmpfs and poudriere's filesystems (lots of them and they are mainly ad-hoc)
* ```df_inode```
  * Calculate accurate filesystem usage percent instead of using rounded one
* ```iostat```
  * Ignore cd and pass devices
* ```if_```
  * Show traffic in bytes, not bits
  * Show traffic in base 1024, not 1000
  * Instead of showing in/out as a -/+ value, show a classic mrtg-like single graph
