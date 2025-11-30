# IPDetails.io API

**Free, Fast, and Accurate IP Geolocation & Threat Intelligence API**

[![IPDetails.io](https://img.shields.io/badge/Status-Online-success)](https://ipdetails.io)
[![API Latency](https://img.shields.io/badge/Latency-~10ms-blue)](https://ipdetails.io)
[![License](https://img.shields.io/badge/License-Free-green)](https://ipdetails.io)

Stop paying for IP data. **[IPDetails.io](https://ipdetails.io)** provides a developer-first API for IP geolocation, WHOIS data, and threat intelligence. No API key required for standard usage, no rate limits, and updated daily.

---

## 🚀 Features

*   **Completely Free:** No credit card or API key required.
*   **Ultra Low Latency:** ~10ms response time with distributed US & EU servers.
*   **Detailed Insights:**
    *   **Geolocation:** Country, City, Region, Coordinates.
    *   **Network Info:** ISP, ASN, Organization.
    *   **Threat Intelligence:** Detect Proxies, VPNs, Tor Nodes, and Hosting/Data Center IPs.
    *   **WHOIS Data:** Abuse contacts and network ownership details.
*   **IPv4 & IPv6 Support:** Full support for both protocols.

---

## ⚡ Quick Start

Get details for any IP address instantly using `curl`:

```bash
curl -s "https://api.ipdetails.io/?ip=72.30.2.43"
```

### Example Response

```json
{
  "abuse_address": "770 BROADWAY FL 4, New York, NY, 10003-9558, US",
  "abuse_email": "network-abuse@cc.yahoo-inc.com",
  "abuse_name": "Oath Holdings Inc.",
  "abuse_phone": "+1-408-349-3300",
  "abuser_score": "0.0001 (Very Low)",
  "autonomous_system_number": 26101,
  "city": "Lockport",
  "company": "Oath Holdings Inc.",
  "country_code": "US",
  "domain": "verizonmedia.com",
  "ip": "72.30.2.43",
  "ip_version": "4",
  "latitude": 43.1721000671387,
  "longitude": -78.6912994384766,
  "network": "72.30.0.0-72.30.255.255",
  "postcode": "14095",
  "rir": "ARIN",
  "state1": "New York",
  "state2": "",
  "timezone": "America/New_York",
  "type": "isp"
}
```

---

## 💻 Integration Examples

Integrate IPDetails.io into your project in under a minute.

### JavaScript / Node.js
```javascript
fetch('https://api.ipdetails.io/?ip=8.8.8.8')
  .then(response => response.json())
  .then(data => console.log(data));
```

### Python
```python
import requests

response = requests.get('https://api.ipdetails.io/?ip=8.8.8.8')
print(response.json())
```

### PHP
```php
$json = file_get_contents('https://api.ipdetails.io/?ip=8.8.8.8');
$details = json_decode($json, true);
print_r($details);
```

### Go
```go
package main

import (
	"fmt"
	"io/ioutil"
	"net/http"
)

func main() {
	resp, _ := http.Get("https://api.ipdetails.io/?ip=8.8.8.8")
	body, _ := ioutil.ReadAll(resp.Body)
	fmt.Println(string(body))
}
```

### Java
```java
import java.net.URI;
import java.net.http.HttpClient;
import java.net.http.HttpRequest;
import java.net.http.HttpResponse;

public class Main {
    public static void main(String[] args) throws Exception {
        HttpClient client = HttpClient.newHttpClient();
        HttpRequest request = HttpRequest.newBuilder()
                .uri(URI.create("https://api.ipdetails.io/?ip=8.8.8.8"))
                .build();

        HttpResponse<String> response = client.send(request, HttpResponse.BodyHandlers.ofString());
        System.out.println(response.body());
    }
}
```

---

## 🛡️ Abuse Contact & Threat Data

IPDetails.io is excellent for security applications. We provide abuse contact information directly in the response, allowing you to automate abuse reporting or block high-risk networks.

```json
"abuse_contact": {
    "name": "Abuse Department",
    "email": "abuse@example.com",
    "phone": "+1-555-0199",
    "address": "123 Tech Street, Silicon Valley, CA"
}
```

---

## 🔗 Links

*   **Website:** [https://ipdetails.io](https://ipdetails.io)
*   **Support:** [support@ipdetails.io](mailto:support@ipdetails.io)

---

&copy; 2025 IPDetails. All rights reserved.

