# Simple Ajax Solution [SASO]
SASO is a MyBB Plugin for [MyBB 1.8.24^](https://github.com/mybb/mybb "MyBB GitHub Repository") that, by using AJAX perform various functions that replace tedious refreshing of the browser whilst expecting _New Posts_, _New Alerts_, _New Mentions_, and other implementations.

The solution also features [Bootstrap Toasts](https://getbootstrap.com/docs/4.3/components/toasts/ "Bootstrap Toasts"), which are more modern and informative.

## Planned Features
This section describes the features that are planned to be implemented, and the section is not a description of the final product nor the goal.

### Bootstrap Toasts
As SASO will be heavily reliant on Toast Notifications, it is optimal to use more informative Toasts to replace or substitute the jGrowl implementation used in MyBB.

1. Include Bootstrap Toast Reliances _(JS/jQuery & CSS)_
To avoid CSS and JS conflicts that could occur between local assets and Bootstrap assets, SASO will ship only the necessary functionality for implementing Bootstrap Toasts.

2. Implement Templates for Toasts
A plan for templates or configuration implementations is not finalized. But through functional analysis, SASO will support these notifications: _Singular New Post on Thread Currently Browsed (Author Avatar)_, _Multiple New Posts on Thread Currently Browsed_, _New Post(s) on a Subscribed Thread_, _New PM_, _New DVZ Mention on Post_, _Received Award_, _Received Reputation_, and possibly more.

### AJAX - New Posts
Any notification that has to do with a new post on the same page that a user is accessing will directly update the page with the latest post, as long as it is possible.

When browsing a thread, periodic checks using AJAX will append new posts as they come in, together with the corresponding notification to the action.
Board Administrators will have the option to choose between two options. 

The first option is an infinite page that will keep adding posts regardless of page limitations. The other option is to use pagination and only use notifications once the page reaches the maximum number of posts

### AJAX - Preview Post
If Board Administrator chooses to, this function can replace the "Preview Post" functionality with a new AJAX-based one that will insert the post as a _fake_ entry on the thread.

_Note: AJAX keeps appending posts above your preview so that what you are seeing is always the most live version of your preview. Once previewing of a post is enabled, the post will keep updating as you work, and if for some reason it stops updating, you have the opportunity to force update the preview._
