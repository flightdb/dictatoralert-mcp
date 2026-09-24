# Dictator Alert MCP — track dictators' planes with AI

The successor to Dictator Alert, rebuilt as an MCP server. Follow the jets of authoritarian leaders, heads of state and royal families from Claude, ChatGPT, Cursor or any MCP-compatible AI assistant, powered by [FlightDB](https://flightdb.org).

Ask in plain language: *"Where has Lukashenko's plane flown this year?"* or *"Which government jets landed in Geneva last month?"* — and get answers from unfiltered ADS-B flight history.

> Independent project. Not affiliated with the original Dictator Alert or its authors.

## Connect

```
https://flightdb.org/mcp
```

Add this URL as a custom MCP connector. Sign in with Google when prompted.

- Transport: Streamable HTTP
- Auth: Google OAuth
- Docs: [flightdb.org/mcp/connect](https://flightdb.org/mcp/connect)

## Why FlightDB

- **Unfiltered ADS-B data** from ADS-B Exchange — no LADD/PIA blocking, unlike FlightRadar24 or FlightAware
- **Full flight history** per aircraft since 2016, not just the last 7 days
- **Registry records** with owner and operator for government and VIP aircraft
- **Airport-level analytics**: who landed where, how often, and for how long

## Regime jets you can track

A sample of state aircraft already in FlightDB:

| Country | Registration | Aircraft | Frequent destinations |
|---|---|---|---|
| Belarus (Lukashenko) | EW-001PB | Boeing 767-32K | Minsk, Abu Dhabi, Beijing |
| Belarus (Lukashenko) | EW-001PA | Boeing 737 BBJ2 | Minsk, St Petersburg, Moscow Vnukovo, Beijing |
| Russia (Putin / state fleet) | RA-96019, RA-96021, RA-96022, RA-96023 | Ilyushin Il-96-300 / 300PU | Moscow Vnukovo, St Petersburg, Dakar, Yerevan, Brazil |
| Turkmenistan | EZ-A777 | Boeing 777-200LR | London Stansted, Paris Orly, Baku |
| Turkmenistan | EZ-A700, EZ-A007 | Boeing 737 BBJ | Munich, Glasgow, London Stansted, Dushanbe |
| Azerbaijan (Aliyev) | 4K-AI001 | Boeing 777-200LR | Baku, Dubai, Italy, Turkey |
| Azerbaijan (Aliyev) | 4K-AI01, 4K-AI08 | Boeing 767 / Airbus A340-600 | Baku, Basel-Mulhouse, Dubai, Tirana |
| Azerbaijan | 4K-AI88, 4K-AI06 | Gulfstream G650 / G550 | Zurich, Dubai, Ibiza, Luton |
| Kazakhstan | UP-A2001 | Airbus ACJ320 | Almaty, Astana, Moscow, Paris |
| Kazakhstan | UP-A3001 | Airbus A330-200 | Astana, Oslo, Basel-Mulhouse, Andrews AFB |
| Saudi Arabia | HZ-HM1 | Boeing 747-400 | Riyadh, Jeddah, Basel-Mulhouse, Morocco |
| Saudi Arabia | HZ-HM3, HZ-HM4, HZ-HM5 | Boeing 787-8 BBJ / 777-300ER | Riyadh, Jeddah, Paris CDG, Switzerland |
| Saudi Arabia | HZ-HMS2 | Airbus A340-200 | Jeddah, London Stansted, Washington Dulles |
| Niger (junta) | 5U-GRN | Boeing 737-700 | Niamey, Basel-Mulhouse, Ouagadougou |

Plus thousands of business jets of oligarchs, royals and billionaires — search by registration, country, owner or ICAO hex code.

## What you can do

- Follow a presidential or government jet's full flight history
- See which countries and airports a regime's aircraft visited, year by year
- Measure how long a plane stayed at an airport (e.g. Geneva, Zurich, Paris Le Bourget, Dubai)
- List all government-owned aircraft of a country
- Find the top routes between two countries
- Spot unusual arrivals at an airport over time

## Tools

| Tool | Description |
|---|---|
| `Flight_list_aircraft` | Aircraft directory — filter by registration, country, owner/operator, ICAO hex |
| `Flight_get_aircraft_from_list` | Aircraft header (registration, type, owner, operator) |
| `Flight_get_aircraft_detail` | Full aircraft profile with all flights and aggregates |
| `Flight_list_flights` | Flights filtered by aircraft, airport, country and date range |
| `Flight_flights_by_year` | Flights per year for an aircraft |
| `Flight_flights_by_country` | Arrival countries per year for an aircraft |
| `Flight_flights_by_distance` | Short / medium / long-haul split per year |
| `Flight_airport_visits` | Visits and length of stay per airport |
| `Flight_visit_history` | Chronological visit timeline |
| `Flight_top_routes` | Most-flown routes between countries or airports |
| `Flight_search_airports` | Find airports by name, city, IATA or ICAO |
| `Flight_get_airport` | Airport details |
| `Flight_airport_stats` | Departures, top destinations and top aircraft at an airport |
| `Flight_airport_arrival_trend` | Arrivals to an airport by day / month / year |
| `Flight_airport_arrivals_by_country` | Arrivals to an airport by origin country |

## Example prompts

- *"Show every flight of Lukashenko's Boeing 767 (EW-001PB) in the last 12 months."*
- *"Which countries did Putin's Il-96 fleet fly to in 2025?"*
- *"How many times did Aliyev's jets land in Switzerland, and how long did they stay?"*
- *"Where has the Turkmenistan Boeing 777 EZ-A777 been since it was delivered?"*
- *"List every aircraft owned by the Government of Kazakhstan and their last flight."*
- *"Which Saudi royal aircraft visited France this year?"*
- *"Track the Niger junta's Boeing 737 5U-GRN — where did it go after the coup?"*
- *"Which government jets landed in Geneva in the last 3 months?"*

## Setup

Add to your MCP client config (Cursor, Claude Desktop, Windsurf, etc.):

```json
{
  "mcpServers": {
    "dictatoralert": {
      "url": "https://flightdb.org/mcp"
    }
  }
}
```

## Keywords

dictator alert, dictator alert successor, dictator plane tracker, dictator jet tracker, authoritarian regime aircraft, presidential jet tracking, government aircraft tracker, head of state flights, Lukashenko plane, Putin plane, Aliyev jet, Turkmenistan presidential plane, Saudi royal flight, VIP jet tracking, oligarch jet tracker, ADS-B, OSINT, flight tracking MCP
