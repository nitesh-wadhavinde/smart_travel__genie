# AI Travel Planner

## Overview

The AI Travel Planner is an agentic application designed to help users plan trips to destinations worldwide. It leverages a combination of Large Language Models (LLMs), various external APIs, and a LangGraph-based agentic workflow to provide comprehensive and detailed travel plans.

## Features

*   **Comprehensive Trip Planning:** Generates detailed day-by-day itineraries, including attractions, restaurants, activities, and transportation options.
*   **Real-Time Data:** Utilizes external APIs to fetch real-time data for weather, places of interest, and currency conversion.
*   **Expense Estimation:** Provides detailed cost breakdowns and per-day expense budgets.
*   **Multiple Travel Plans:** Generates two travel plans, one for generic tourist spots, and another for off-beat locations.
*   **Flexible LLM Support:** Supports both Groq and OpenAI LLMs.
*   **Modular Design:** Features a modular architecture with clearly separated components for model loading, tool integration, and API handling.
*   **API Integration:** Uses FastAPI to provide a RESTful API endpoint for easy integration with front-end applications.
*   **Configurable:** Uses YAML-based configuration for easy customization.
*   **Document Export:** Allows users to save travel plans as Markdown files.

## Technologies Used

*   **LangGraph:** Orchestrates the agentic workflow and conversation flow.
*   **LangChain:** Provides an interface for interacting with LLMs and tools.
*   **LLMs:** Groq and OpenAI.
*   **FastAPI:** Creates the RESTful API.
*   **Streamlit:** Creates an interactive web application
*   **Tools:**
    *   Weather Information (OpenWeatherMap API)
    *   Place Search (Google Places API, Tavily Search API)
    *   Expense Calculator
    *   Currency Converter (ExchangeRate-API)
*   **Other Libraries:** Pydantic, PyYAML, python-dotenv, requests
*   **Mermaid:** Visualize the LangGraph Graph

## Setup

### Prerequisites

*   Python 3.10+
*   API keys for:
    *   Groq or OpenAI
    *   Google Places API
    *   OpenWeatherMap API
    *   ExchangeRate-API
    *   Tavily API (optional, for fallback place search)

### Installation

1.  Clone the repository:

    ```bash
    git clone <repository_url>
    cd AI_TRIP_PLANNER
    ```

2.  Create a virtual environment (recommended):

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Linux/macOS
    venv\Scripts\activate  # On Windows
    ```

3.  Install the dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4.  Configure the environment variables:

    *   Create a `.env` file in the root directory.
    *   Add your API keys to the `.env` file:

        ```
        OPENAI_API_KEY=<your_openai_api_key>
        GROQ_API_KEY=<your_groq_api_key>
        GOOGLE_API_KEY=<your_google_api_key>
        GPLACES_API_KEY=<your_google_places_api_key>
        OPENWEATHERMAP_API_KEY=<your_openweathermap_api_key>
        EXCHANGE_RATE_API_KEY=<your_exchange_rate_api_key>
        TAVILAY_API_KEY=<your_tavilay_api_key> # optional
        ```

### Running the Application

1.  Start the FastAPI backend:

    ```bash
    python main.py
    ```

2.  (Optionally) Run the Streamlit frontend:

    ```bash
    streamlit run streamlit_app.py
    ```

## Usage

1.  Access the API endpoint (e.g., `http://localhost:8000/query`) to send travel planning queries.
2.  (If using the Streamlit frontend) Enter your query in the input box and submit.

