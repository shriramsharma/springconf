## Java  Caching

#### SpringOne2GX 2015: Wednesday 4:30PM

* JSR-107 JCache
  Temporary in-memory caching of java objects.
* A TCK
* No capacity control.
* JSR-107 is "Store By Value" by default
** The cache must copy the value and put it in the cache.
* `javax-cache` and implementation `org.ehcache`
* JSR-107 is multithreaded. Stick only immutable objects.


