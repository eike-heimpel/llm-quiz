# LLM Quiz Application

An interactive quiz application powered by GPT-4 with text-to-speech capabilities and Wikipedia-grounded answers.

## Features

- Dynamic question generation using GPT-4
- Wikipedia-grounded answers for accuracy
- Multiple difficulty levels and categories
- Text-to-speech support for accessibility
- Interactive UI with immediate feedback
- Mobile-responsive design

## Project Structure

```
.
├── backend/               # FastAPI backend
│   ├── __init__.py
│   ├── main.py           # Main FastAPI application
│   ├── llm_integration.py # LLM integration for question generation
│   ├── speech.py         # Text-to-speech functionality
│   └── requirements.txt  # Python dependencies
└── frontend/             # SvelteKit frontend
    ├── src/
    │   ├── lib/
    │   │   └── api.ts   # API integration
    │   ├── routes/
    │   │   ├── +page.svelte    # Main quiz interface
    │   │   └── +layout.svelte  # App layout
    │   └── app.css      # Global styles
    └── package.json     # Node.js dependencies
```

## Setup

### Backend Setup

1. Create a Python virtual environment:
   ```bash
   cd backend
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Create a .env file:
   ```bash
   cp .env.example .env
   ```

4. Add your OpenAI API key to the .env file:
   ```
   OPENAI_API_KEY=your_api_key_here
   ```

5. Start the backend server:
   ```bash
   uvicorn main:app --reload
   ```

The backend will be available at http://localhost:8000

### Frontend Setup

1. Install dependencies:
   ```bash
   cd frontend
   npm install
   ```

2. Start the development server:
   ```bash
   npm run dev
   ```

The frontend will be available at http://localhost:5173

## Usage

1. Open your browser and navigate to http://localhost:5173
2. Select your preferred difficulty level and category
3. Toggle voice narration on/off using the speaker button
4. Read or listen to the question
5. Select your answer
6. Submit your answer to see if you're correct
7. Click "Next Question" to continue

## API Documentation

The backend API documentation is available at http://localhost:8000/docs when the backend server is running.

## Development

### Backend Development

- The backend is built with FastAPI
- Question generation uses GPT-4 via the OpenAI API
- Text-to-speech is implemented using gTTS
- All questions are grounded in Wikipedia articles for accuracy

### Frontend Development

- Built with SvelteKit for optimal performance
- Styled with Tailwind CSS
- Fully responsive design
- Accessibility features including ARIA labels and keyboard navigation
- Voice interaction support

## License

MIT License
