# Sample Codes

## Python

```python
import requests

ip_address = "{IP-ADDRESS}"
url = f"https://freeipapi.com/api/json/{ip_address}"

response = requests.get(url)
data = response.json()

print(data)
```

## PHP

```php
<?php

$ipAddress = "{IP-ADDRESS}";
$url = "https://freeipapi.com/api/json/$ipAddress";

$response = file_get_contents($url);
$data = json_decode($response, true);

print_r($data);
```

## Java

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.net.HttpURLConnection;
import java.net.URL;

public class Main {
    public static void main(String[] args) throws IOException {
        String ipAddress = "{IP-ADDRESS}";
        String urlString = "https://freeipapi.com/api/json/" + ipAddress;

        URL url = new URL(urlString);
        HttpURLConnection connection = (HttpURLConnection) url.openConnection();
        connection.setRequestMethod("GET");

        BufferedReader reader = new BufferedReader(new InputStreamReader(connection.getInputStream()));
        StringBuilder response = new StringBuilder();
        String line;
        while ((line = reader.readLine()) != null) {
            response.append(line);
        }
        reader.close();

        System.out.println(response.toString());
    }
}
```

## JavaScript (Node.js)

```javascript
const axios = require('axios');

const ipAddress = "{IP-ADDRESS}";
const url = `https://freeipapi.com/api/json/${ipAddress}`; // to get specific ip's info
// const url = `https://freeipapi.com/api/json/`; // to get current request's ip info

axios.get(url)
    .then(response => {
        const data = response.data;
        console.log(data);
    })
    .catch(error => {
        console.error(error);
    });
```

## JavaScript (jQuery)

```javascript
const ipAddress = "{IP-ADDRESS}";
const url = `https://freeipapi.com/api/json/`; // to get current request's ip info
// const url = `https://freeipapi.com/api/json/${ipAddress}`; // to get specific ip's info

$.get(url, function (data) {
    console.log(data);
});
```

## Ruby

```ruby
require 'net/http'
require 'json'

ip_address = "{IP-ADDRESS}"
url = URI.parse("https://freeipapi.com/api/json/#{ip_address}")
http = Net::HTTP.new(url.host, url.port)
http.use_ssl = true

request = Net::HTTP::Get.new(url.request_uri)
response = http.request(request)
data = JSON.parse(response.body)

puts data
```

## C#

```csharp
using System;
using System.Net.Http;
using System.Threading.Tasks;

class Program
{
    static async Task Main()
    {
        string ipAddress = "{IP-ADDRESS}";
        string url = $"https://freeipapi.com/api/json/{ipAddress}";

        using (HttpClient client = new HttpClient())
        {
            HttpResponseMessage response = await client.GetAsync(url);
            string responseBody = await response.Content.ReadAsStringAsync();

            Console.WriteLine(responseBody);
        }
    }
}
```

## Rust

```rust
use reqwest;

#[tokio::main]
async fn main() -> Result<(), Box> {
    let ip_address = "{IP-ADDRESS}";
    let url = format!("https://freeipapi.com/api/json/{}", ip_address);

    let response = reqwest::get(&url).await?.text().await?;
    println!("{}", response);

    Ok(())
}
```

## Golang

```go
package main

import (
	"fmt"
	"io/ioutil"
	"net/http"
)

func main() {
	ipAddress := "{IP-ADDRESS}"
	url := fmt.Sprintf("https://freeipapi.com/api/json/%s", ipAddress)

	response, err := http.Get(url)
	if err != nil {
		fmt.Println(err)
		return
	}
	defer response.Body.Close()

	body, err := ioutil.ReadAll(response.Body)
	if err != nil {
		fmt.Println(err)
		return
	}

	fmt.Println(string(body))
}
```