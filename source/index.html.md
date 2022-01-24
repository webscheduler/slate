---
title: Web Scheduler Local v19e21171-07a0-4f46-9eeb-429b2bc422be
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: false
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="web-scheduler-local">Web Scheduler Local v19e21171-07a0-4f46-9eeb-429b2bc422be</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

# Introduction
What does your API do?

# Overview
Things that the developers should know about

# Authentication
What is the preferred way of using the API?

# Error Codes
What errors and status codes can a user expect?

# Rate limit
Is there a limit to the number of requests an user can send?

Base URLs:

* <a href="http://localhost:8082">http://localhost:8082</a>

 License: 

# Authentication

- HTTP Authentication, scheme: apikey 

<h1 id="web-scheduler-local-default">Default</h1>

## Every

<a id="opIdEvery"></a>

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:8082/v1/schedules/every?apiKey=b1b0d2d0cb1ef52a96cb5e66a66738bca95b4b8d8fbf0820b459f8bbfa8d484c \
  -H 'Content-Type: text/plain'

```

```http
POST http://localhost:8082/v1/schedules/every?apiKey=b1b0d2d0cb1ef52a96cb5e66a66738bca95b4b8d8fbf0820b459f8bbfa8d484c HTTP/1.1
Host: localhost:8082
Content-Type: text/plain

```

```javascript
const inputBody = '{
  "interval": "year",
  "path": "/webhook",
  "name": "Every 3"
}';
const headers = {
  'Content-Type':'text/plain'
};

fetch('http://localhost:8082/v1/schedules/every?apiKey=b1b0d2d0cb1ef52a96cb5e66a66738bca95b4b8d8fbf0820b459f8bbfa8d484c',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'text/plain'
}

result = RestClient.post 'http://localhost:8082/v1/schedules/every',
  params: {
  'apiKey' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'text/plain'
}

r = requests.post('http://localhost:8082/v1/schedules/every', params={
  'apiKey': 'b1b0d2d0cb1ef52a96cb5e66a66738bca95b4b8d8fbf0820b459f8bbfa8d484c'
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'text/plain',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://localhost:8082/v1/schedules/every', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://localhost:8082/v1/schedules/every?apiKey=b1b0d2d0cb1ef52a96cb5e66a66738bca95b4b8d8fbf0820b459f8bbfa8d484c");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"text/plain"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://localhost:8082/v1/schedules/every", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /v1/schedules/every`

> Body parameter

```
interval: year
path: /webhook
name: Every 3

```

<h3 id="every-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|apiKey|query|string|true|none|
|body|body|string|true|none|

<h3 id="every-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
apikey, apikey, apikey
</aside>

## Delete Job

<a id="opIdDeleteJob"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE http://localhost:8082/v1/schedules/aQYh78xwr1

```

```http
DELETE http://localhost:8082/v1/schedules/aQYh78xwr1 HTTP/1.1
Host: localhost:8082

```

```javascript

fetch('http://localhost:8082/v1/schedules/aQYh78xwr1',
{
  method: 'DELETE'

})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://localhost:8082/v1/schedules/aQYh78xwr1',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.delete('http://localhost:8082/v1/schedules/aQYh78xwr1')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://localhost:8082/v1/schedules/aQYh78xwr1', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://localhost:8082/v1/schedules/aQYh78xwr1");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "http://localhost:8082/v1/schedules/aQYh78xwr1", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /v1/schedules/aQYh78xwr1`

<h3 id="delete-job-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
apikey, apikey, apikey
</aside>

## Create Schedule

<a id="opIdCreateSchedule"></a>

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:8082/v1/schedules \
  -H 'Content-Type: text/plain' \
  -H 'X-API-Key: 8f8679cc07d2b17c7dd19f5d2086d2b1'

```

```http
POST http://localhost:8082/v1/schedules HTTP/1.1
Host: localhost:8082
Content-Type: text/plain

X-API-Key: 8f8679cc07d2b17c7dd19f5d2086d2b1

```

```javascript
const inputBody = '{
  "name": "Event name",
  "path": "/webhooks/reminder",
  "when": "2021-11-08T12:59:33.874Z",
  "data": {
    "eventId": "111"
  }
}';
const headers = {
  'Content-Type':'text/plain',
  'X-API-Key':'8f8679cc07d2b17c7dd19f5d2086d2b1'
};

fetch('http://localhost:8082/v1/schedules',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'text/plain',
  'X-API-Key' => '8f8679cc07d2b17c7dd19f5d2086d2b1'
}

result = RestClient.post 'http://localhost:8082/v1/schedules',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'text/plain',
  'X-API-Key': '8f8679cc07d2b17c7dd19f5d2086d2b1'
}

r = requests.post('http://localhost:8082/v1/schedules', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'text/plain',
    'X-API-Key' => '8f8679cc07d2b17c7dd19f5d2086d2b1',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://localhost:8082/v1/schedules', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://localhost:8082/v1/schedules");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"text/plain"},
        "X-API-Key": []string{"8f8679cc07d2b17c7dd19f5d2086d2b1"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://localhost:8082/v1/schedules", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /v1/schedules`

> Body parameter

```
name: Event name
path: /webhooks/reminder
when: 2021-11-08T12:59:33.874Z
data:
  eventId: "111"

```

<h3 id="create-schedule-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|X-API-Key|header|string|true|none|
|body|body|string|true|none|

<h3 id="create-schedule-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
apikey, apikey, apikey
</aside>

## Get Jobs

<a id="opIdGetJobs"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:8082/v1/schedules?fromDate=2020-10-04T17%3A00%3A29.996Z

```

```http
GET http://localhost:8082/v1/schedules?fromDate=2020-10-04T17%3A00%3A29.996Z HTTP/1.1
Host: localhost:8082

```

```javascript

fetch('http://localhost:8082/v1/schedules?fromDate=2020-10-04T17%3A00%3A29.996Z',
{
  method: 'GET'

})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://localhost:8082/v1/schedules',
  params: {
  'fromDate' => 'string'
}

p JSON.parse(result)

```

```python
import requests

r = requests.get('http://localhost:8082/v1/schedules', params={
  'fromDate': '2020-10-04T17:00:29.996Z'
})

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://localhost:8082/v1/schedules', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://localhost:8082/v1/schedules?fromDate=2020-10-04T17%3A00%3A29.996Z");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://localhost:8082/v1/schedules", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /v1/schedules`

<h3 id="get-jobs-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|fromDate|query|string|true|none|

<h3 id="get-jobs-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
apikey, apikey, apikey
</aside>

## Get Job

<a id="opIdGetJob"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:8082/v1/schedules/TMAe3VqcC1

```

```http
GET http://localhost:8082/v1/schedules/TMAe3VqcC1 HTTP/1.1
Host: localhost:8082

```

```javascript

fetch('http://localhost:8082/v1/schedules/TMAe3VqcC1',
{
  method: 'GET'

})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://localhost:8082/v1/schedules/TMAe3VqcC1',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('http://localhost:8082/v1/schedules/TMAe3VqcC1')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://localhost:8082/v1/schedules/TMAe3VqcC1', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://localhost:8082/v1/schedules/TMAe3VqcC1");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://localhost:8082/v1/schedules/TMAe3VqcC1", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /v1/schedules/TMAe3VqcC1`

<h3 id="get-job-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
apikey, apikey, apikey
</aside>

