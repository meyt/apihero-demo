Version 2.1
-----------

### General Changes

<ul>
<li>
All methods are now available under the /2.1/ path, new properties will only be returned if the /2.1/ version of a method is called.
</li>
<li>
Limited support for [writing via the API], restricted to [comments].
</li>
<li>
/users/{ids}/top-answer-tags and users/{ids}/top-question-tags are now vectorized.
</li>
<li>
`write_access` and `private_info` scopes added to [OAuth flows].
</li>

  [writing via the API]: /docs/write
  [comments]: /docs/types/comment
  [OAuth flows]: /docs/authentication