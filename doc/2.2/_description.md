Stack Exchange API v2.2
-----------------------

This is the documentation for the v2.2 Stack Exchange API (with both [authentication] and [write] support). If you have additional questions, or believe you have encountered a bug, don’t hesitate to post a question on [Stack Apps].

If your application is in a runnable state (even a beta one), Stack Apps is also the place to [list it].

General
-------

Applications should be registered on [Stack Apps][1] to get a request key. Request keys grant more requests per day, and are necessary for using access\_tokens created via [authentication].

All API responses are [JSON], we do support [JSONP] with the `callback` query parameter. Every response in the API is returned in a common [“wrapper” object], for easier and more consistent parsing.

Additionally, all API responses are compressed. The `Content-Encoding` header is always set, but some proxies will strip this out. The proper way to decode API responses can be found [here].

API usage is subject to a [number of throttles]. In general, applications should strive to make as few requests as possible to satisfy their function.

API responses are heavily cached. Polling for changes should be done sparingly in any case, and polling at a rate faster than once a minute (for semantically identical requests) is considered abusive.

Developers can trim API responses down to just the fields they are interested in using [custom filters]. Many types have fields that are not normally returned (question bodies, for example) that can likewise be requested via a custom filter.

There are a few methods which require that the application be acting on behalf of a user in order to be invoked. For authentication purposes, the Stack Exchange API [implements OAuth 2.0][authentication] (templated on Facebook’s implementation in pursuit of developer familiarity).

A number of methods in the Stack Exchange API accept dates as parameters and return dates as properties, the format of these dates is [consistent and documented]. The cliff-notes version is, all dates in the Stack Exchange API are in [unix epoch time].

Unless otherwise noted, the maximum size of any page is `100`, any `{ids}` pa

  [authentication]: /docs/authentication
  [write]: /docs/write
  [Stack Apps]: http://stackapps.com
  [list it]: http://stackapps.com/questions/7/how-to-list-your-application-library-wrapper-here
  [1]: http://stackapps.com/apps/oauth/register
  [JSON]: http://en.wikipedia.org/wiki/JSON
  [JSONP]: http://en.wikipedia.org/wiki/JSONP
  [“wrapper” object]: /docs/wrapper
  [here]: /docs/compression
  [number of throttles]: /docs/throttle
  [custom filters]: /docs/filters
  [consistent and documented]: /docs/dates
  [unix epoch time]: http://en.wikipedia.org/wiki/Unix_time