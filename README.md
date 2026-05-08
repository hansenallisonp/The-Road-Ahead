# The-Road-Ahead
By: Allison Hansen
This repository is created to compare major tire brands (Michelin, Continental, Goodyear, Bridgestone) using public/open data. 

**Running the Road Ahead:** This application can be launched from the python notebook included in this repository and only requires inserting an OpenAI API key. 

**Application Description:** The Road Ahead compares major tire brands (Michelin, Continental, Goodyear, Bridgestone) on their positioning, competition and standings in electronic vehicles and autonomous vehicles. I am inspired by the future of vehicles & tires; riding in a Waymo for the first time in San Fransisco and starting this project by reading about how tires should be adapted to the weight and constant use of electric and autonomous vehicles. I also wanted to consider Michelin's core values, respect for the environment when choosing an application design. 

The application features KPI averaged scores per brand, 4 tabs: radar plot, scorecard per brand, news articles scraped as data sources, and an AI analyst, as well as a drill down by dimension. 
The five dimensions included are EV Tire Innovation, AV Integration, Sustainability Commitment, Strategic Partnerships, and Innovation Pipeline. The dimensions are scored by GPT-4o-mini with a prompt to score each one from 0 to 100 based only on what appears in the text, the scores are entirely GPT’s interpretation of what the scraped text says about each brand so noteably for this example, they reflect media coverage and public statements more than facts. 

**Business Impact:**
With more thorough data, this application has the ability to demonstrate how Michelin compares to competitors in the future of electric vehicles and autonomous vehicles and provide continuous updates and alerts of new articles in the space. 

**Data Sources:** The data is collected using web scraping from articles and news sources from 3 sources, Google News RSS, Wikipedia, and the website of each Brand for news and press releases. The web scraping is extremely limited and should be considered an example, not comprehensive. For a production ready application, more data as well as from additional sources and equitable data collection should be considered. The scoring method as currently designed will create lower scores when less evidenece is present thus potentially skewing scores on brands with more articles collected. 

**Tools & Tech:** 
Google colab notebook - code base
Gradio & plotly - UI interface and plots 
Requests, feedparser, BeautifulSoup - web scraping 
GPT-4o-mini, LangChain, LangGraph - scores and AI agent 
Claude - application design & code assistance

**Additional Application Notes:**
This application is not Michelin favored but is sourced solely by extremely limited web scraping. Results & scores should not be considered fact but examples. 
Early on in the design process, I was exploring open source datasets and found the National Highway Traffic Safety Administration Datasets and API, I noticed Michelin did not have any recalls until 2020-2024 dataset, no recalls in 2025! It was a slightly difficult API to use considering time constraints; required calling vehicles, when I tried lists of popular vehicles the quantity of data was not there but I would’ve liked to explore this dataset more with more time.

**Application Brainstorming & Other Ideas:**
Before designing the application I wanted to consider: Who would be the customer / user? Why would they want this application? What would this application provide? What data can I find open source? 
A few other possible application ideas were: Stock ticker + sentiment analysis, Supply chain tracker + news analysis, Customer sentiment analysis + weather / geography layer (would require customer location, hard if not impossible to find open source) 

**Areas for Improvement / Next Steps:**
- Potentially make the “AI Agent” a RAG model, this was something I debated heavily in the design
- Collect more data, not just articles 
- Ensure that amount of data (esp. articles) collected per brand is equitable to eliminate GPT scores favoring brands that are more well represented 
- Create alerts for competitor action within the space 

This information is also included in slide format in the ppt in this repository.  
