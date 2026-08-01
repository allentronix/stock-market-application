# Query Data from the Web - Citi Technology Software Development

## Overview

This project was completed as part of the **Citi Technology Software Development Virtual Experience Program on Forage**.

The project focuses on building a Java application that retrieves real-time market data from a web API, processes the response, and stores the collected information for further use.

The application connects to the **Twelve Data API** to retrieve the current price of the **DIA ETF**, captures the timestamp of each request, and stores the results in a queue.

---

## Project Objectives

The goal of this task was to create a program that can:

- Connect to an external web API
- Retrieve financial market data
- Process API responses
- Store collected data efficiently
- Handle repeated data requests over time

---

## Features

- Retrieves DIA price data using the Twelve Data API
- Uses an API key stored securely as an environment variable
- Captures the current timestamp for every data request
- Stores each price update in a queue
- Repeats data collection at regular intervals
- Displays collected data and queue size in the console

---

## Technologies Used

- **Java**
- **REST API**
- **HTTP Requests**
- **JSON Data Processing**
- **Queue Data Structure**
- **Google Colab**
- **Twelve Data API**

---

## Application Workflow

The application follows these steps:

1. The program loads the Twelve Data API key from an environment variable.
2. A request is sent to the Twelve Data API endpoint:
https://api.twelvedata.com/price?symbol=DIA&apikey=YOUR_API_KEY


3. The API returns the latest DIA price.
4. The program extracts the price from the response.
5. A timestamp is generated using the current system time.
6. The price and timestamp are stored as a data point in a queue.
7. The process repeats after a fixed time interval.

---

## Example Output

API key found: True

Added data point: price=420.15, timestamp=2026-08-01T04:00:00
Current queue size: 1

Added data point: price=420.20, timestamp=2026-08-01T04:00:15
Current queue size: 2

Added data point: price=420.18, timestamp=2026-08-01T04:00:30
Current queue size: 3

Finished collecting data.

## Project Structure


Query-Data-From-The-Web/
│
├── App.java # Main Java application
└── README.md # Project documentation


---

## Implementation Details

### API Integration

The application communicates with the Twelve Data API using Java's built-in networking libraries.

The program sends HTTP GET requests and receives JSON responses containing the latest DIA price.

### Data Storage

Each retrieved price is stored as an object containing:

- Price value
- Timestamp of retrieval

These objects are stored inside a Java `Queue` data structure.

### Scheduling

The application pauses between requests to simulate periodic data collection and avoid excessive API calls.

---

## Skills Demonstrated

Through this project, I practiced:

- Java programming
- Working with external APIs
- HTTP communication
- JSON response handling
- Data structures and queues
- Environment variable management
- Debugging and testing applications

---

## About the Program

This project was completed as part of the **Citi Technology Software Development Virtual Experience Program on Forage**.

It demonstrates the process of creating a small software component that communicates with external services and processes real-world data.

---

## Disclaimer

This is a personal project completed for educational purposes as part of a virtual experience program. It is not an official Citi software system or production application.
