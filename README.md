# FlightAI – AI-Powered Airline Assistant

FlightAI is an intelligent airline assistant powered by Large Language Models (LLMs) that can answer travel-related queries, retrieve real-time ticket prices using tool calling, generate AI travel posters for destinations, and respond with natural-sounding voice output.

The application combines conversational AI, database integration, AI image generation, and text-to-speech into a single interactive web interface.

---

## Features

- AI-powered airline assistant
- Function (Tool) Calling with Groq LLM
- SQLite database integration for ticket prices
- AI-generated destination travel posters
- Natural voice responses using ElevenLabs
- Interactive Gradio web interface
- Automatic tool execution based on user queries
- Secure API key management using environment variables

---

## Tech Stack

- Python
- Groq API
- Llama 3.3 70B Versatile
- SQLite
- Gradio
- ElevenLabs
- Flux Kontext API
- Pillow (PIL)
- Requests
- python-dotenv

---

## Project Workflow

1. User enters a travel-related question.
2. The request is sent to the Groq LLM.
3. If ticket pricing is required, the LLM automatically invokes the database tool.
4. The application retrieves the ticket price from SQLite.
5. The LLM generates a natural language response.
6. ElevenLabs converts the response into speech.
7. Flux AI generates a travel poster for the destination.
8. The Gradio interface displays the chat, voice response, and generated image.

```
              User
                │
                ▼
        Gradio Web Interface
                │
                ▼
          Groq LLM (Llama 3.3)
                │
      ┌─────────┴─────────┐
      │                   │
      ▼                   ▼
Function Calling      Normal Chat
      │
      ▼
SQLite Ticket Database
      │
      ▼
Price Returned to LLM
      │
      ▼
Final AI Response
      │
 ┌────┴───────────────┐
 ▼                    ▼
ElevenLabs       Flux Kontext API
(Text-to-Speech) (AI Travel Poster)
      │                    │
      └──────────┬─────────┘
                 ▼
           Gradio Output
```

---

## Project Structure

```
FlightAI/
│
├── main.py
├── flight.db
├── requirements.txt
├── .env
├── .gitignore
└── README.md
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/yourusername/FlightAI.git
```

Move into the project directory

```bash
cd FlightAI
```

Create a virtual environment

```bash
python -m venv .venv
```

Activate the virtual environment

### Windows

```bash
.venv\Scripts\activate
```

### macOS/Linux

```bash
source .venv/bin/activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Environment Variables

Create a `.env` file in the project root.

```env
GROQ_API_KEY=your_groq_api_key
FLUX_API_KEY=your_flux_api_key
ELEVENLABS_API_KEY=your_elevenlabs_api_key
```

---

## Usage

Run the application

```bash
python main.py
```

The application launches a Gradio interface in your browser.

Example questions:

```
What is the ticket price to Paris?
```

```
How much does a return ticket to Tokyo cost?
```

```
Ticket price for London
```

---

## Example Output

For supported destinations, FlightAI will:

- Retrieve the ticket price from the SQLite database
- Generate a concise AI response
- Produce natural speech
- Generate an AI travel poster for the destination

---

## Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Core application |
| Groq API | LLM inference |
| Llama 3.3 70B Versatile | Conversational AI & tool calling |
| SQLite | Ticket price database |
| Gradio | Interactive web interface |
| ElevenLabs | Text-to-speech |
| Flux Kontext API | AI image generation |
| Pillow | Image processing |
| Requests | API communication |
| python-dotenv | Environment variable management |

---

## Future Improvements

- Real-time flight APIs
- Flight booking functionality
- Flight schedules and availability
- Multi-city itinerary planning
- User authentication
- Conversation history
- Hotel recommendations
- Weather information for destinations
- Streaming chatbot responses
- Multi-language support

---

## License

This project is intended for educational and portfolio purposes.
