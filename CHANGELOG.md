CHANGELOG
=========

v1.2.0
------
* Roll back the use of psycopg2 connection pools. (See [tilequeue/#149](https://github.com/tilezen/tilequeue/pull/149) and [#62](https://github.com/tilezen/tileserver/pull/62))

v1.1.0
------
* Add support for meta-tiles to group multiple formats per tile coordinate into a single ZIP archive (See [#53](https://github.com/tilezen/tileserver/issues/53))
* Improve performance of GeoJSON and TopoJSON format generation by using ujson (See [tileserver/#139](https://github.com/tilezen/tilequeue/issues/139))
* Add support for psycopg2 connection pools (See [#59](https://github.com/tilezen/tileserver/pull/59) and [tilequeue/#141](https://github.com/tilezen/tilequeue/issues/141))

v1.0.1
------
* Improvements to documentation.
* Update to account for change to function signature which changed to accomodate priority queues. See [#54](https://github.com/tilezen/tileserver/pull/54) for more information.

v1.0.0
------
* Update process_cord function call to account for new return values (size logging).
* Update the sample configuration to reflect new options.
* Add pyclipper dependency to requirements.

v0.7.0
------
* Removed TileStache and Pillow dependencies
* Updated other dependency versions
* Update function calls to support latest tilequeue changes, including support for buffered MVT tile extents
* Add cors config option

v0.6.1
------
* Allow configuration of formats to handle

v0.6.0
------
* Update calls for layer specific store changes
* Support post process functions
* Metatile at z16

v0.5.1
------

* Store additional formats rendered to support a request. Also send the job to the queue, if one is configured, for "full" rendering. [Issue](https://github.com/mapzen/tileserver/pull/14).

v0.5.0
------
* Update to support date- and hash-prefixed stores and S3 buckets.
* Normalise layer creation so that tiles are only generated with a full set of layers. These will be stored and any subset of layers that the client requested will be filtered from it. This improves consistency when many layers have interdependent post-processing steps.

v0.4.2
------
* Update implementation of processing cached tile from store
* Ensure properties are strings from cached tile before re-formatting

v0.4.1
------
* Allow threaded server configuration for local development

v0.4.0
------
* Do not insert coords greater than z20 into toi

v0.3.0
------
* Use store to serve dynamic layer requests

0.2.0
-----
* Stable
