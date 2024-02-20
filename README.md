# Prom-Ua Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Prom-Ua Scraper](https://oxylabs.io/products/scraper-api/ecommerce/prom-ua?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Prom-Ua website effortlessly. This brief guide showcases how Prom-Ua Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Prom-Ua results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Prom-Ua page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://prom.ua/kosmeticheskie-sredstva-po-uhodu-za-kozhej-litsa'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/prom-ua-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n        <!doctype html>\n        <html\n            lang='ru'\n            data-pds-color-scheme='ligh ... </html>",
      "created_at": "2024-02-20 12:44:01",
      "updated_at": "2024-02-20 12:44:06",
      "page": 1,
      "url": "https://prom.ua/kosmeticheskie-sredstva-po-uhodu-za-kozhej-litsa",
      "job_id": "7165687541243338753",
      "status_code": 200
    }
  ]
}
```
With our Prom-Ua Scraper, you're able to seamlessly gather public data from any Prom-Ua webpage. Gather necessary product information such as product images, manufacturer details, or stock count to streamline your market research and outpace your competition. If you find yourself needing assistance, please feel free to reach out to our dedicated support team through live chat or shoot us an email at hello@oxylabs.io.