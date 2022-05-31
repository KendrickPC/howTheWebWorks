# How Web Works Exercise

### Part One: Solidify Terminology
In your own terms, define the following terms:

1. What is HTTP?

The Hypertext Transfer Protocol is an application protocol for distributed, collaborative, hypermedia information systems that allows users to communicate data on the World Wide Web.

2. What is a URL?

Short for uniform resource locator, a URL identifies specific pages on the Internet. To find the URL of the page you're currently reading, just check the address bar at the top of your browser. The address updates automatically as you move from one page to another.

3. What is DNS?

The domain name system (i.e., “DNS”) is responsible for translating domain names into a specific IP address so that the initiating client can load the requested Internet resources. The domain name system works much like a phone book where users can search for a requested person and retrieve their phone number.

4. What is a query string?

A querystring is a set of characters input to a computer or Web browser and sent to a query program to recover specific information from a database.

5. What are two HTTP verbs and how are they different?

The primary or most-commonly-used HTTP verbs (or methods, as they are properly called) are POST, GET, PUT, PATCH, and DELETE. These correspond to create, read, update, and delete (or CRUD) operations, respectively. There are a number of other verbs, too, but are utilized less frequently.

6. What is an HTTP request?

An HTTP request is made by a client, to a named host, which is located on a server. The aim of the request is to access a resource on the server. To make the request, the client uses components of a URL (Uniform Resource Locator), which includes the information needed to access the resource.

7. What is an HTTP response?

An HTTP response is made by a server to a client. The aim of the response is to provide the client with the resource it requested, or inform the client that the action it requested has been carried out; or else to inform the client that an error occurred in processing its request.

8. What is an HTTP header? Give a couple examples of request and response headers you have seen.

HTTP headers let the client and the server pass additional information with an HTTP request or response. An HTTP header consists of its case-insensitive name followed by a colon (:), then by its value. Whitespace before the value is ignored.

HTTP headers can be classified into four types:
  HTTP Request Header
  HTTP Response Header
  HTTP General Header
  HTTP Entity Header

9. What are the processes that happen when you type “http://somesite.com/some/page.html” into a browser?

  turn "somesite.com" into 123.45.67.89
  connect 123.45.67.89
  On port 80 (the default)
  Using HTTP Protocol
  Ask for /some/page.html 

### Part Two: Practice Tools
1. Using curl, make a GET request to the icanhazdadjoke.com API to find all jokes involving the word “pirate”

[How to use CURL](https://flaviocopes.com/http-curl/)
```console
$ curl -H "Accept: application/json" "https://icanhazdadjoke.com/search?term=pirate"
```

2. Use dig to find what the IP address is for icanhazdadjoke.com

```console 
dig icanhazdadjoke.com

icanhazdadjoke.com.	83	IN	A	104.21.37.176
icanhazdadjoke.com.	83	IN	A	172.67.211.64
```

3. Make a simple web page and serve it using python3 -m http.server. Visit the page in a browser.

```console
cd [root folder]
python3 -m http.server
```
Go into browser and type the url localhost:8000

### Part Three: Explore Dev Tools
1. Build a very simple HTML form that uses the GET method (it can use the same page URL for the action) when the form is submitted.

2. Add a field or two to the form and, after submitting it, explore in Chrome Developer tools how you can view the request and response headers.
[How to view HTTP headers in Google Chrome?](https://mkyong.com/computer-tips/how-to-view-http-headers-in-google-chrome/)

3. Edit the page to change the form type to POST, refresh in the browser and re-submit. Do you still see the field in the query string? Explore in Chrome how you can view the request and response headers, as well as the form data.

### Part Four: Explore the URL API

At times, it’s useful for your JavaScript to look at the URL of the browser window and change how the script works depending on parts of that (particularly the query string).

[Read about the URL API](https://developer.mozilla.org/en-US/docs/Web/API/URL)

Try some of the code examples in the Chrome Console so that you can get comfortable with the basic methods and properties for instances of the URL class.

Inside google chrome's developer console:

```js
// https://www.espn.com/nba/
const url = new URL('/nba', 'https://www.espn.com/');
console.log(url.hostname); // "www.espn.com"
console.log(url.pathname); // "/nba"
```
