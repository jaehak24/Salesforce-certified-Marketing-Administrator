# Salesforce Object Query Language

Use the Salesforce Object Query Language(SOQL) to search your organization's Salesforce data for specific information. SOQL is similar to the SELECT statement in the widely used Structured Query Language(SQL) but is designed specifically for Salesforce data.

With SOQL, you can construct simple but powerful query strings in several environments
* Using the <b><u>queryString</u></b> parameter of a SOAP API <u>query ()</u> call. 


## Query()
executes a query against the specified object and returns data that matches the stated conditions.


### 예제 synatx
> QueryResult= connection. query(string queryString);


### usage of <u>query()</u>
use the query() call to retrieve data from an object. When a client applicaiton invokes the query() call, it passes in a query expression that specifies the objet to query, the field to retrieve, and any conditions that determine wheter a given object qualifies. For detail about the syntax and rules used for queries, see the Salesforce SOQL and SOSL Reference Guide: SOQL SELECT Syntax.

Upon invocation, the API executes the query against the specified object, cache the results of the query on the API, and returns the query response object <b>QueryResult</b>. The client application

