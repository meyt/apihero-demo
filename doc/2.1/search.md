Searches a site for any questions which fit the given criteria.

This method is intentionally quite limited. For more general searching, you should use a proper internet search engine restricted to the domain of the site in question.

At least one of `tagged` or `intitle` must be set on this method. `nottagged` is only used if `tagged` is also set, for performance reasons.

`tagged` and `nottagged` are semi-colon delimited list of tags. At least 1 tag in `tagged` will be on each returned question if it is passed, making it the OR equivalent of the AND version of `tagged` on [/questions].

The sorts accepted by this method operate on the follow fields of the [question object]:

-   **activity** – `last_activity_date`
-   **creation** – `creation_date`
-   **votes** – `score`
-   **relevance** – matches the relevance tab on the site itself
    -   Does not accept `min` or `max`

`activity` is the default sort.
It is possible to [create moderately complex queries] using `sort`, `min`, `max`, `fromdate`, and `todate`.

This method returns a list of [questions][question object].

  [/questions]: /docs/questions
  [question object]: /docs/types/question
  [create moderately complex queries]: /docs/min-max