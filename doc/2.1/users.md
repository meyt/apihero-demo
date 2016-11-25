Returns all users on a site.

This method returns a list of [users].

The sorts accepted by this method operate on the follow fields of the [user object][users]:

-   **reputation** – `reputation`
-   **creation** – `creation_date`
-   **name** – `display_name`
-   **modified** – `last_modified_date`

`reputation` is the default sort.
It is possible to [create moderately complex queries] using `sort`, `min`, `max`, `fromdate`, and `todate`.

The `inname` parameter lets consumers filter the results down to just those users with a certain substring in their display name. For example, [`inname=kevin`] will return all users with both users named simply “Kevin” or those with Kevin as one of (or part of) their names; such as “Kevin Montrose”.

  [users]: /docs/types/user
  [create moderately complex queries]: /docs/min-max
  [`inname=kevin`]: http://api.stackexchange.com/docs/users#order=desc&sort=reputation&inname=kevin&filter=default&site=stackoverflow

