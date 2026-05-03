Group project proposal
Chosen paper: Mancilla, Bouloumis & Goguikian (2026). Non-Convex Portfolio Optimization via Energy-Based Models: A Comparative Analysis Using the Thermodynamic HypergRaphical Model Library (THRML) for Index Tracking. arXiv:2601.07792
Project overview
We aim to replicate and extend the THRML index tracker from the paper by (Mancilla et al., 2026).
•	Replication: We produced the paper’s cardinality constrained index tracking approach, which uses energy minimisation on an Ising Hamiltonian.
•	Extension: Rather than using the VIX based regime-switching model, we use a two-state Hidden Markov Model (HMM) which is estimated from S&P500 returns history data. The prices were procured from yfinance and transformed into returns.

Explanation of the code
1.	We import the libraries and download the top 100 S&P500 price data (2010-2025).
2.	Apply a train/test split: train(2010-2022), test(2023-2025)
3.	Score the stocks and build the Ising model.
4.	We make sure to run quarterly rebalancing using both the VIX and HMM methods.
5.	The code also produces performance tables and charts.
The libraries:
Yfinance: for stock price data
Panda and numpy: Data manipulation
Hmmlearn: to fit the 2-state Gaussian HMM model
Matplotlib and seborn: for the charts and visualisation
Requests, beautifulsoup, and lxml: to scrape the S&P500 data

Group members
Sakhile Buthelezi
Phenyo Thato Molete
Samson Mashabane
Palesa Letho
