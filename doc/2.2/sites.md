Returns all sites in the network.

This method allows for discovery of new sites, and changes to existing ones. Be aware that unlike normal API methods, this method should be fetched very infrequently, it is very unusual for these values to change more than once on any given day. It is suggested that you cache its return for at least one day, unless your app encounters evidence that it has changed (such as from the [/info method]).

The `pagesize` parameter for this method is unbounded, in acknowledgement that for many applications repeatedly fetching from `/sites` would complicate start-up tasks needlessly.

This method returns a list of [sites].

  [/info method]: /docs/info
  [sites]: /docs/types/site