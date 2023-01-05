----
HttpValueCollection vs NameValueCollection. When creating an instance of NameValueCollection with new(), ToString() method doesn't return collection, but when creating an instance of NameValueCollection using HttpUtility.ParseQueryString(), ToString() method returns the collection as a query string with all the names and values. These links explain why that is.
* https://stackoverflow.com/questions/7514461/httpvaluecollection-and-namevaluecollection
* https://stackoverflow.com/questions/19723931/tostring-of-copied-namevaluecollection-doesnt-output-desired-results
----

