# Frog Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Frog Scraper](https://oxylabs.io/products/scraper-api/ecommerce/frog?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Frog website effortlessly. This brief guide showcases how Frog Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Frog results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Frog page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.frog.ee/en/category/2359-top-50-best-sellers'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/frog-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en-us\"><head><meta charset=\"utf-8\"><script src=\"https://pagead2.googlesyn ... </html>",
      "created_at": "2024-02-20 12:41:12",
      "updated_at": "2024-02-20 12:41:38",
      "page": 1,
      "url": "https://www.frog.ee/en/category/2359-top-50-best-sellers",
      "job_id": "7165686832426918913",
      "status_code": 200
    }
  ]
}
```
With our Frog Scraper, you can seamlessly gather public data from any Frog blog post or forum thread. Assemble the necessary data like post date, comments, or content to understand user behavior and remain competitive in your market. If you require further help, our support team is available on live chat, or you can email us at hello@oxylabs.io.