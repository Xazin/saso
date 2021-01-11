# Simple Ajax Solution [SASO]
SASO is a MyBB Plugin for [MyBB 1.8.24^](https://github.com/mybb/mybb "MyBB GitHub Repository") that by using AJAX perform various functions that replace tedious refreshing of the browser whilst expecting _New Posts_, _New Alerts_, _New Mentions_, and other implementations.

The solution also features Bootstrap Toasts, that are more modern and informative.

## Planned Features
This section describes the features that are planned to be implemented, the section is not a description of the final product nor the goal.

### Bootstrap Toasts
As SASO will be heavily reliant on Toast Notifications, it is optimal to use more informative Toasts to replace or substitute the jGrowl implementation used in MyBB.

1. Include Bootstrap Toast Reliances _(JS/jQuery & CSS)_
Instead of including the whole Bootstrap Library, only the necessary functionality will be included.

2. Implement Templates for Toasts
It is not yet planned which templates or configurations for the toast templates and themes that need to be implemented so far, though it is _surmised_ that these notifications be supported: _Singular New Post on Thread Currently Browsed (Author Avatar)_, _Multiple New Posts on Thread Currently Browsed_, _New Post(s) on a Subscribed Thread_, _New PM_, _New DVZ Mention on Post_, _Received Award_, _Received Reputation_, and possibly more.

### AJAX - New Posts
Any notification that has to do with a new post on the same page that a user is accessing, will directly update the page with the new post, as long as it is possible.

When _you_ are on a thread, other than receiving a _notification_ that a new post has been made the post is _automatically added to the page_ so that the user can read the new post without refreshing the page. In case that the amount of _posts_ on a _thread_ reaches the maximum amount for each _page_, the pagination is updated and the notification will include information that new posts can be found on the _next_ page.
