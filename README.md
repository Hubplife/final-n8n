**the repetitive task being automated:**
We are automatizing making a decision about buying a stock of the given symbol. The AI is supposed to decide for the user if it is worth to buy it.

**the workflow logic:**
We use a form submission to collect data from the user. The user enters only the stock symbol they are interested in, and this value is sent to the HTTP Request node. The HTTP Request node connects to the Alpha Vantage API and retrieves weekly stock price data using an API key, which allows n8n to access the information. Because the dataset contains too much data, a JavaScript script filters the results and keeps only the data from the last five weeks. Next, the filtered data is sent to an AI model, which answers the question: “Is it worth buying stock of this company?” We use an AI model accessed through the Groq API. After that, another JavaScript script converts the JSON string into a JavaScript object, making it possible to pass the data to the “Send a Message” node. The message is then sent to a Discord bot, which responds to the user. The final message contains the stock name, the AI’s recommendation on whether it is worth buying, a risk scale, and a short summary explaining the decision.

**The role of AI:**
AI has a huge role in the automatized project. It replaces a human in analyzing process and decison makeing. Its task is to decide if the client should buy a stock or not. 

**How the system can be executed and tested:** To test the system user have to fill the form with the stock symbol. It is assured, that user writes correct proper symbol. A few seconds later, there will be messege from discord bot, which conveys AI information. There need to be all information that are sent to the bot.
