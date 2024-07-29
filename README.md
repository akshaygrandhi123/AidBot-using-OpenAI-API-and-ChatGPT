# AidBot: E-commerce Customer Support Chatbot

AidBot is an automated customer support chatbot designed to assist customers with their e-commerce orders on platforms like Amazon or Flipkart. It provides efficient, 24/7 support by handling routine inquiries and streamlining the customer service experience.

## Features

- Greets customers and collects order numbers
- Identifies common issues (refunds, returns, delivery problems, etc.)
- Provides immediate solutions for simple issues
- Escalates complex problems to human representatives
- Collects necessary information for follow-up calls
- Generates JSON summaries of customer interactions

## Prerequisites

Before running AidBot, ensure you have the following installed:

- Python 3.7 or higher
- pip (Python package installer)

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/AidBot.git
   cd AidBot
   ```

2. Install the required libraries:
   ```
   pip install openai python-dotenv panel
   ```

## OpenAI API Key

To use the OpenAI API, you need to obtain an API key:

1. Sign up for an account at [OpenAI](https://openai.com/)
2. Navigate to the API section and create a new API key
3. Create a `.env` file in the project root directory
4. Add your API key to the `.env` file:
   ```
   OPENAI_API_KEY=your_api_key_here
   ```

## Usage

1. Run the Python script:
   ```
   python aidbot.py
   ```

2. Interact with AidBot using the provided chat interface

## How it Works

1. **API Setup**: The code uses the OpenAI API to generate responses. It loads the API key from the `.env` file using the `dotenv` library.

2. **Helper Functions**: 
   - `get_completion()`: Sends a single prompt to the OpenAI API
   - `get_completion_from_messages()`: Sends a list of messages to the OpenAI API

3. **Chat Interface**: The `collect_messages()` function handles user input and bot responses. It uses the Panel library to create an interactive chat interface.

4. **Context and Knowledge Base**: The bot's knowledge and behavior are defined in the `context` variable. This includes information about common issues and how to handle customer interactions.

5. **User Interaction**: 
   - The bot greets the customer and asks for their order number
   - It identifies the customer's issue and attempts to resolve it
   - For unresolved issues, it offers to arrange a call with a human representative

6. **JSON Summary**: After the conversation, the bot can generate a JSON summary of the customer interaction, including details like order number, issue type, resolution status, and more.

## Customization

You can customize AidBot's behavior by modifying the `context` variable in the script. This allows you to add or change the types of issues it can handle and adjust its conversational style.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT License](LICENSE)

## Acknowledgments

- OpenAI for providing the GPT model
- Panel library for the interactive interface
