# AI-Trading-Floor
Here's a small project of mine which is a demonstration of my recent learnings from MCP Servers, clients and OpenAI Agents SDK. This is a trading floor run by 4 AI agents - Warren, George, Ray, Cathie - who leverages 3 custom servers using FastMCP. Account server provides tools to get the current state of the user's accounts. Market Server provides the tool to fetch the share price. Push server uses provides the tool to send a push notification using Pushover.

This trading floor has 4 agents who continuously make trades depending on share prices. They also send me a push notification to my phone/laptop when they make a trade. I have also added some additional logging in the web applicaiotn so that the user can see what's going on in the backend. There is sqlite memory set up in the backend to store the trades of each agents and to store the user's account information.

Since this a demo, I have used the free plan of the Polygon API which only gives me information about yesterday's closing price, thus the agents make trading decisions based on yesterday's closing price. I would love to deploy this publicly but the beauty of this trading floor is that it keeps running which can raise OpenAI API costs for me. Thank you for taking a look at it and credit to Ed Donner's Agentic AI course that helped me build this. 

Run the frontend with `uv run app.py` and run the backend with `uv run trading_floor.py`. Since there is memory, If you want to have the agents start from scratch again and reset their trades then run `uv run reset.py`



