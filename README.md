# Air Quality Alert

A Java command line tool that checks the air quality where you are and tells you in plain words whether it's a good day to head outside.

## Project Goal

People who like being outside often have no idea whether the air is safe for a run or a walk until they go looking it up. That usually means opening an app or website and searching for their location every single time, so most people just skip it. Smoke from wildfires and everyday pollution can make anyone feel sick, so knowing the air quality shouldn't take that much effort.

This project solves that by automatically detecting the user's location, pulling the current air quality from the free Open Meteo Air Quality API, and showing a clear warning when the air gets worse than a level the user picks.

## MVP 

The first working version will:

- Detect the user's approximate location using IP-API
- Get current air quality data for that location from the Open Meteo Air Quality API
- Read the US Air Quality Index (AQI) and translate it into plain words (Good, Moderate, Unhealthy, etc.)
- Let the user choose a warning level and show a clear warning and health tip when the air is worse than that level
- Handle basic errors like no internet connection or invalid input

## Future Plans (for version 2+)

- Look up air quality for any location by name, not just the user's own
- Give advice based on the user's planned activity and their sensitivity to air pollution
- Include weather and temperature details along with the air quality reading
- Show tomorrow's air quality forecast so users can plan ahead

## Tech Stack

- **Java 25:** the programming language for the whole project
- **java.net.http (HttpClient):** sends requests to the Open Meteo and IP-API web APIs
- **Gson:** reads the JSON data that the APIs send back
- **IO.readln:** reads what the user types, like their warning level
- **java.time:** handles the time each air quality reading was taken
- **JUnit:** tests that the AQI translation and warnings work correctly

## Data Sources

- **Open Meteo Air Quality API:** provides current air quality data. Free, no API key, returns JSON.
- **IP-API:** finds the user's approximate location. Free for noncommercial use, no API key, returns JSON.
