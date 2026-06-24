# Source: https://python.datalumina.com/libraries-apis/working-with-apis

## 

[​](https://python.datalumina.com/#what-is-an-api)

What is an API?

An API (Application Programming Interface) is like a waiter at a restaurant. You tell it what you want, and it brings you the data. But APIs do more than just fetch information. They’re the bridges that connect your code to other systems. With APIs, you can:

- Pull customer data from your CRM (Salesforce, HubSpot)
- Get order information from Shopify or WooCommerce
- Send messages through Slack or email services
- Use AI models from OpenAI or Anthropic

In the context of AI, APIs are essential. They let you connect AI capabilities to real business data and systems.

## 

[​](https://python.datalumina.com/#your-first-api-call)

Your first API call

Let’s get real weather data using a free weather API:

```
import requests

# We need coordinates to get weather data
latitude = 48.85   # Paris latitude
longitude = 2.35   # Paris longitude

# Build the API URL with our parameters
url = f"https://api.open-meteo.com/v1/forecast?latitude={latitude}&longitude={longitude}&current=temperature_2m"

# Make the request
response = requests.get(url)
data = response.json()

print(data)
```

First install requests: `pip install requests`

## 

[​](https://python.datalumina.com/#understanding-the-response)

Understanding the response

The API sends back data in JSON format (like a Python dictionary):

```
{
    'latitude': 48.84,
    'longitude': 2.36,
    'timezone': 'GMT',
    'elevation': 46.0,
    'current_units': {
        'temperature_2m': '°C'
    },
    'current': {
        'time': '2025-08-01T08:30',
        'temperature_2m': 20.0
    }
}
```

The temperature is nested inside `current`, so to get it:

```
temperature = data['current']['temperature_2m']
print(f"Temperature in Paris: {temperature}°C")
# Output: Temperature in Paris: 20.0°C
```

**What is JSON?** JSON (JavaScript Object Notation) is just a way to structure data, similar to CSV or Excel files. While CSV stores data in rows and columns, JSON uses key-value pairs like Python dictionaries.

## 

[​](https://python.datalumina.com/#extract-what-you-need)

Extract what you need

Now you can pull out specific information:

```
import requests

def get_weather(latitude, longitude):
    response = requests.get(f"https://api.open-meteo.com/v1/forecast?latitude={latitude}&longitude={longitude}&current=temperature_2m,wind_speed_10m")
    data = response.json()
    return data['current']['temperature_2m']

# Get temperature for different cities
paris_temp = get_weather(48.85, 2.35)
london_temp = get_weather(51.50, -0.12)
tokyo_temp = get_weather(35.68, 139.69)

print(f"Paris: {paris_temp}°C")
print(f"London: {london_temp}°C")
print(f"Tokyo: {tokyo_temp}°C")
```

## 

[​](https://python.datalumina.com/#how-it-works)

How it works

1. **You send a request** to the API’s URL with parameters (like coordinates)
2. **The API processes** your request and finds the data
3. **You receive JSON data** back with the information
4. **You extract** the specific parts you need

The pattern is always the same: connect to an API, send requests, get data back, use it in your code. APIs are how modern software talks to each other.

[**Working with data**\\ \\ Process data efficiently with pandas](https://python.datalumina.com/libraries-apis/working-with-data)

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/libraries-apis/working-with-apis.mdx)

[Import packages](https://python.datalumina.com/libraries-apis/importing-modules) [Working with data](https://python.datalumina.com/libraries-apis/working-with-data)

Ctrl+I