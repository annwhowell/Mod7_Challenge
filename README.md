# Mod7_Challenge - Analyisis of an ETF and an ETF portfolio from SQL databae

This program pulls data from a SQL database to analyze results for an ETF called PYPL and plot daily returns
and cumulative returns. It also compares four ETFs (PYPL, GDOT, GS, SQ) in a portfolio and plots
daily returns and cumulative returns for the 4 ETFs. Finally, Voila was used to create a web page with results.



# Required programs and libraries

To install from terminal:
'''
conda install -c pyviz hvplot geoviews
'''

Libraries called in program:
'''
import numpy as np
import pandas as pd
import hvplot.pandas
import sqlalchemy
'''

# Data Sources
Data is pulled using sqlite from a SQL database provided in the Resources file

'''
database_connection_string = 'sqlite:///etf.db'

engine = sqlalchemy.create_engine(database_connection_string)
'''


# Sections

**Section 1:** Queries the database to pull and examine data for PYPL etf; creates an hvplot for daily returns

![PYPL Daily Returns 2016-2020](PYPL_daily_returns_graph.png)

**Section 2:** For PYPL, calculates cumulative return and creates a plot
    
![PYPL Cumulative Returns](PYPL_cumulative_returns_graph.png)    

**Section 3:** Narrows data to meet specification such as when PYPL closing price is greater than 200
    
**Section 4:** Join data for four ETFs (PYPL, GDOT, GS, SQ) to compare daily and cumulative returns
![Cumulative Returns for GDOT, PYPL, SQ, GS](four_funds_cumulative_returns.png)


**Additional Output** Webpage created by Voila from the Git Bash terminal

Commands to run voila and create a webpage of etf_analyzer.ipynb

![Voila terminal commands](voila_terminal.png)

Voila creates a webpage on the local host computer

![Voila Webpage](proof_of_voila_webpage.png)

    
# Creator
Program by Ann Howell with guidance from Rice FinTech Bootcamp

# License
MIT