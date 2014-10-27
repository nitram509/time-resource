# Time Resource

Implements a resource that reports new versions on a configured interval. The
interval can be arbitrarily long.

This resource is built to satisfy "trigger this build at least once every 5
minutes," not "trigger this build on the 10th hour of every Sunday." That
level of precision is better left to other tools.


## Source Configuration

* `interval`: *Required.* The interval on which to report new versions.


## Behavior

### `check`: Report the current time.

Returns a new version only if it has been longer than `interval` since the
given version, or if there is no version given.


### `in`: Report the given time, or current time.

If triggered by `check`, returns the original version as the resulting
version. Otherwise, returns the current time as the resulting version.

#### Parameters

*None.*


### `out`: Not implemented.

If you can figure out what updating time could possibly mean in this
universe, submit a PR. With tests.

#### Parameters

*None.*
