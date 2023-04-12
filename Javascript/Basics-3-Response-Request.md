# Response and Request  

The **Response** and **Request** objects are part of the **Fetch API**, a browser API for making network requests. 
They are used to represent the response received from a server and the request that was made respectively.

The Request object represents the request that will be sent to the server. It contains information about the 
request, such as the URL, method, headers, and body data. You can create a new Request object by passing a URL 
or a Request object to the **fetch()** method.

The Response object represents the response returned from the server. It contains information about the response,
such as the status code, headers, and body data. You can get a Response object from a **fetch()** request, and you 
can read the response data using methods such as json(), text(), or blob().  

## Request

The Request object in JavaScript provides several properties that carry important information about the HTTP request 
being made, including:  

 - **method:** The HTTP method used for the request (e.g. GET, POST, etc.).
 - **url:** The URL of the resource being requested.
 - **headers:** An object containing the HTTP headers of the request.
 - **body:** The body of the request (for POST, PUT, and PATCH requests).  


## Response

On the other hand, the Response object contains properties and methods that are used to handle the response of an HTTP 
request. The most important properties of the Response object include:  

 - **ok:** A boolean that indicates whether the request was successful (response status in the range of 200-299) or not.
 - **status:** The HTTP status code returned by the server.
 - **statusText:** The status message returned by the server.
 - **headers:** An object containing the headers of the response.
 - **body:** A ReadableStream object representing the body of the response.  

In addition to these properties, the Response object also has several methods that can be used to handle the response, 
such as **json()**, which parses the response body as JSON and returns the result as a JavaScript object, and text(), which 
reads the response body as text.  

