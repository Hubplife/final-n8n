# final-n8n
https://didactic-memory-x5gv7qv46qgph6q4q-5678.app.github.dev/home/workflows

the repetitive task being automated:
We are automatizing making a decision about buying a stock of the given company.
the workflow logic:
We use form submision to collect the data from the user. The user write only the name of the stock, he is interested in, and then this input is sent to the HTTP request node. The HTTP request node go to this website and collects basic information about the stock change from every week. Later the Javascript code filters collected data to show only those from last five weeks. After that, the data is sent to the AI  model, which is obliged to answer the question "Is it worth to buy stocks of this company?". Then...

The role of AI:
AI is the biggest decision maker in this project. Its task is to decide if the client should buy a stock or not.

How the system can be executed and tested:
Firstly, the wrokflow must be executed and the proper link must be written in the browser. Then the user writes the stock data he is into. After that,...