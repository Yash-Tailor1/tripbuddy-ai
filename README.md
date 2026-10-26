# ✈️ TripBuddy-AI

### A Multi-Agent AI Travel Planner Using LangGraph

TripBuddy-AI is an AI-powered travel planning application that uses a **multi-agent architecture built with LangGraph** to generate personalized travel plans from natural language requests.

Simply describe your travel requirements, and TripBuddy-AI coordinates specialized AI agents to help organize your journey.

## 🌐 Live Demo

**Try TripBuddy-AI here:** [Launch TripBuddy-AI](https://tripbuddy-ai-1.onrender.com)

Explore AI-powered travel planning with a multi-agent architecture built using LangGraph.

## 🚀 Features

### ✈️ Flight Search
- Searches for relevant flight information based on the origin and destination.
- Considers user-provided travel requirements.
- Helps users explore suitable flight options.

### 🏨 Hotel Discovery
- Finds relevant hotel recommendations for the destination.
- Provides hotel names, locations, descriptions, and useful travel information.
- Helps travelers explore accommodation options based on their requirements.

### 🗺️ AI-Powered Itinerary Generation
- Creates personalized, day-by-day travel itineraries.
- Suggests sightseeing spots, activities, and food recommendations.
- Organizes daily schedules and local transportation suggestions.

### 💰 Budget-Conscious Travel Planning
- Considers the user's travel budget and preferences.
- Helps organize flights, accommodation, and activities into a practical travel plan.
- Supports personalized recommendations based on trip requirements.

### 🤖 Multi-Agent Architecture
- Uses **LangGraph** to coordinate specialized AI agents.
- Separates flight search, hotel discovery, itinerary generation, and final response preparation.
- Combines agent outputs into a unified travel plan.

### 📄 Downloadable Travel Plan
- Generates a travel plan that can be downloaded as a PDF.
- Makes it easier to save, review, and share travel details.

## 🏗️ Multi-Agent Architecture

TripBuddy-AI uses a sequential multi-agent workflow orchestrated by LangGraph.

```text
                    User Request
                         │
                         ▼
                ┌─────────────────┐
                │  Flight Agent   │
                │ Flight Search   │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │   Hotel Agent   │
                │ Hotel Discovery │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Itinerary Agent │
                │ Daily Planning  │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │   Final Agent   │
                │ Plan Generation │
                └────────┬────────┘
                         │
                         ▼
                 Personalized
                   Travel Plan
```

### Workflow

1. **User Request:** The user describes the destination, duration, budget, and travel preferences in natural language.
2. **Flight Agent:** Searches for relevant flight information.
3. **Hotel Agent:** Discovers suitable accommodation options.
4. **Itinerary Agent:** Creates a personalized itinerary based on the trip requirements.
5. **Final Agent:** Combines the available information into a structured travel plan.
6. **PDF Generation:** Makes the travel plan available as a downloadable document.

## 🛠️ Tech Stack

- **Python** — Core application development
- **LangGraph** — Multi-agent workflow orchestration
- **LangChain** — LLM integration and tool orchestration
- **LLM APIs** — AI-powered reasoning and content generation
- **FastAPI** — Backend API *(if enabled in your implementation)*
- **Tavily** — Web search capabilities *(if configured in your implementation)*

## 💬 Example Request

> Plan a 5-day Dubai trip from Mumbai, including flights, hotels, sightseeing, and a budget-friendly itinerary.

TripBuddy-AI processes the request through its specialized agents to create a consolidated travel plan.

## ⚙️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Yash-Tailor1/TripBuddy-AI.git
cd TripBuddy-AI
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it:

**macOS / Linux**
```bash
source .venv/bin/activate
```

**Windows**
```bash
.venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the project root and add the API keys required by your implementation.

```env
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
```

Add any other required environment variables based on your configuration. Never commit real API keys or secrets to GitHub.

### 5. Run the Application

Use the entry point configured in your repository. For example, if your application exposes a FastAPI instance at `app.main:app`, run:

```bash
uvicorn app.main:app --reload
```

Open the API documentation at:

```text
http://127.0.0.1:8000/docs
```

*Adjust the startup command if your repository uses a different entry point.*

## 🌐 Deployment

TripBuddy-AI is deployed on Render and accessible online.

**Live Application:** [Launch TripBuddy-AI](https://tripbuddy-ai-1.onrender.com)

The application is hosted on Render, with environment variables configured for the deployed service.

Before deployment:

- Install dependencies from `requirements.txt`.
- Configure the required API keys securely.
- Set the correct application startup command.
- Verify that external APIs and agent workflows operate correctly in the deployed environment.

## 🔒 Security

- Store API keys in environment variables.
- Keep `.env` out of version control.
- Use `.gitignore` to exclude secrets, virtual environments, and generated files.
- Configure production secrets through your hosting provider.

## 🔮 Future Enhancements

- Real-time flight price and availability integration.
- Hotel booking platform integrations.
- Interactive maps and route optimization.
- Persistent trip history and user preferences.
- More advanced budget estimation and expense breakdowns.
- Parallel agent execution where appropriate.
- Enhanced itinerary export and sharing.

## 👨‍💻 Author

**Yash Tailor**

AI Engineer | Agentic AI | LLM Applications

GitHub: [@Yash-Tailor1](https://github.com/Yash-Tailor1)

---

*TripBuddy-AI — Smarter travel planning powered by multi-agent AI.*
