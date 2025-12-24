# Sports Bot using Gemini

A conversational AI bot that answers sports-related questions using Google's Gemini API. This project demonstrates the integration of generative AI for creating a domain-specific conversational assistant.

## Project Description

The Sports FAQ Bot leverages Google's Gemini AI to provide accurate, conversational responses to questions about various sports. It covers rules, tournaments, players, and general sports knowledge with a natural, engaging interface.

## Features

- **Natural Conversational Interface**: Maintains conversation context and provides follow-up questions
- **Multi-Sport Coverage**: Knowledgeable about football, cricket, basketball, tennis, and general sports topics
- **Two Interaction Modes**: 
  - Full conversational mode with memory
  - Quick Q&A mode for simple questions
- **Error Handling**: Graceful management of API errors and unclear queries
- **Easy Deployment**: Optimized for Google Colab and local execution

### Installation

1. Clone the repository:
```bash
git clone https://github.com/nyairopetronilla/Sport-Bot-using-Gemini.git
cd Sport-Bot-using-Gemini
```

2. Install the required package:
```bash
pip install google-generativeai
```

3. Get your Gemini API key:
   - Visit [Google AI Studio](https://aistudio.google.com/app/apikey)
   - Sign in with your Google account
   - Create a new API key

### Basic Usage

```python
import google.generativeai as genai
from getpass import getpass

# Configure with your API key
api_key = getpass("Enter your Gemini API key: ")
genai.configure(api_key=api_key)

# Initialize and run the bot
from sport_bot import ConversationalSportsBot
bot = ConversationalSportsBot()
bot.chat_loop()
```

### Running in Google Colab

The code is fully compatible with Google Colab. Simply copy the Python code into a Colab notebook cell, run it, and enter your API key when prompted.

## How It Works

### Core Components

1. **Gemini AI Integration**: Uses Google's `gemini-2.5-flash` model for fast, accurate responses
2. **Conversation Management**: Maintains context across multiple exchanges for coherent dialogue
3. **System Prompts**: Guides the AI to respond in a friendly, sports-expert tone
4. **Error Handling**: Manages API errors and provides user-friendly messages

### Available Commands

During conversation:
- Type your sports questions naturally
- Type `quit`, `exit`, or `bye` to end the session
- Type `back` in Q&A mode to return to main conversation

## Example Interactions

```
You: What are the rules of football?
SportsBot: Football (soccer) is played with 11 players per team... What specific aspect of the rules would you like to know more about?

You: Who won the last cricket world cup?
SportsBot: The last ICC Cricket World Cup in 2023 was won by Australia... Are you interested in cricket history or current tournaments?

You: Compare basketball and tennis
SportsBot: While both are popular sports, basketball is a team sport with 5 players... Which sport are you more interested in playing?
```

## Configuration

The bot uses `gemini-1.5-flash` by default. To use a different model:

```python
# In the ConversationalSportsBot class initialization
self.model = genai.GenerativeModel('gemini-1.5-pro')  # Alternative model
```

## Requirements

- `google-generativeai` Python package
- Active internet connection for API calls
- Valid Gemini API key

## Limitations

- Requires an internet connection for API access
- Dependent on Gemini API availability and rate limits
- May not have information on very recent sports events
- Accuracy is dependent on the underlying AI model

## Future Enhancements

Potential improvements for this project include:

- Integration with live sports data APIs
- Multi-language support
- Voice interface capabilities
- Sports trivia and quiz modes
- Web or mobile application interface

## License

This project is intended for educational purposes. Users are responsible for complying with Google's Gemini API terms of service.

## Support

For issues or questions, please check:
1. Your Gemini API key validity and quota
2. Internet connectivity
3. Python environment compatibility

## Acknowledgments

- Google for providing the Gemini AI API
- The open-source community for AI and Python resources

---
*This project was developed for educational purposes to demonstrate practical AI application development.*
```
