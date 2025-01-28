# crypto-ai-agent
A simple AI agent designed to fetch real-time Bitcoin prices and handle language translation requests, ensuring English remains the primary communication language.

This project is designed to implement a cryptocurrency-focused AI agent that provides insights based on cryptocurrency data. The notebook `crypto_agent.ipynb` contains code for the agent.

## Features

The LLM agent has access to 2 tools namely fetch_crypto_price and translate_text.
1. fetch_crypto_price - This function uses CoinMarketCap's API (see here for more information - https://coinmarketcap.com/api/documentation/v1/ ) to get the real-time Bitcoin (or any other cryptocurrency) price.
2. translate_text - This function translates input text from any language to English language.
   
## Getting Started

### Prerequisites

Make sure you have the following installed:

- Python 3.8 or later (This notebook was created using Python 3.11.0)
- Jupyter Notebook
- Required Python libraries:
  ```bash
  pip install -r requirements.txt
  ```

### Usage

1. Run the last cell that contains the main function to converse with the agent, once you are done type 'quit' or 'exit' to end the conversation.
2. You can see sample conversation flows in the notebook :
   a. First conversation flow asks all questions in english and gets appropriate responses from the AI Agent :
      AI Agent: Hello! How can I assist you today?
      You: What is Bitcoin?
      AI Agent: Bitcoin is a decentralized digital currency that allows for peer-to-peer transactions without the need for intermediaries like banks. It was       created in 2009 by an individual or group of individuals using the pseudonym Satoshi Nakamoto.
      You: What is its current price?
      AI Agent: The current price of Bitcoin is 102225.264.
      You: How much money will be needed to buy 5 bitcoins?
      AI Agent: The current price of Bitcoin is 102225.26482329183 USD. To buy 5 Bitcoins, you would need 5 x 102225.26482329183 = 510112.6224164586 USD.
      You: What is indian rupees to usd exchange rate?
      AI Agent: The Indian rupee (INR) to US dollar (USD) exchange rate is subject to fluctuations and can vary depending on various market and economic factors. As of now, the exchange rate is around 75.50 INR per USD.
      You: If the exchange rate currently is 1 USD = 85 INR, then what is bitcoin's price in indian rupees?
      AI Agent: The price of Bitcoin in Indian Rupees is 102366.69834756962 * 85 = 8705119.999999999
      You: Thank you for your assistance today.
      AI Agent: You're welcome! It was my pleasure to assist you. If you have any more questions or need further assistance, feel free to ask!
      You: exit
      AI Agent: Goodbye!

   b. Second conversation flow is in Spanish :
      AI Agent: Hello! How can I assist you today?
      You: Hola
      AI Agent: Hello! How can I assist you today?
      You: ¿cuál es el precio de Bitcoin hoy?
      AI Agent: The current price of Bitcoin is 102,446.151 USD.
      You: ¿Y cuál es el precio de Ethereum?
      AI Agent: The current price of Ethereum is 3162.595 USD.
      You: Gracias por su ayuda hoy.
      AI Agent: You're welcome! It was my pleasure to assist you today.
      You: quit
      AI Agent: Goodbye!

## Limitations

1. The user query has to be very clear, otherwise LLM generates erratic messages.
2. Multiple actions maybe not processed correctly for eg. What is bitcoin and ethereum's price? (2 actions need to be performed, call fetch_crypto_price for 4. bitcoin and call fetch_crypto_price for ethereum, but the llm may output only bitcoin's price correctly)
4. When the agent doesn't know the answer, it might keep generating imaginary actions or outputs wrong answers.


## Contact

Further improvements are in progress.
For any questions or suggestions, please contact [shreekodate21@gmail.com].

