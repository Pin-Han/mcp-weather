# MCP Weather

A weather information application that uses Anthropic Claude's LLM to query US weather data through the National Weather Service (NWS) API. This project is based on Anthropic's official MCP (Model Context Protocol) examples.

## Overview

This project consists of two main components:

- A server that provides weather tools via the Model Context Protocol (MCP)
- A client that connects to the server and uses Anthropic Claude to process user queries

## Features

- Get weather alerts for any US state
- Get weather forecasts for any US location by coordinates
- Natural language interface powered by Anthropic Claude 3.5 Sonnet

## Prerequisites

- Node.js (v16 or higher)
- An Anthropic API key

## Setup

1. Clone this repository

   ```
   git clone https://github.com/your-username/mcp-weather.git
   cd mcp-weather
   ```

2. Install dependencies for both client and server

   ```
   # Install client dependencies
   cd client
   npm install

   # Install server dependencies
   cd ../server
   npm install
   ```

3. Create a `.env` file in the project root with your Anthropic API key
   ```
   ANTHROPIC_API_KEY=your_anthropic_api_key_here
   ```

## Usage

1. Start the server

   ```
   cd server
   npm start
   ```

2. In a separate terminal, run the client and provide the path to the server

   ```
   cd client
   npm start ../server/build/index.js
   ```

3. Enter your weather queries in natural language, for example:
   - "What's the weather forecast for New York City?"
   - "Are there any weather alerts in California?"
   - "What will the temperature be in Chicago tomorrow?"

## Available Weather Tools

- `get-alerts`: Get weather alerts for a US state (requires two-letter state code)
- `get-forecast`: Get weather forecast for a location (requires latitude and longitude)

## Security Note

This application requires an Anthropic API key to function. Never commit your `.env` file or expose your API key in public repositories.

## License

[MIT License](LICENSE)
