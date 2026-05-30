# The Book Club: Quantitative Finance & Econometrics Vault

Welcome to **The Book Club**, a highly rigorous personal study repository dedicated to deep-diving into seminal academic textbooks across financial engineering, econometrics, Bayesian data analysis, and financial machine learning. 

Rather than treating these legendary texts as passive reading material, this vault is built for **active replication**. Every chapter studied is backed by implementing mathematical equations from scratch, coding pricing and simulation models, visualizing complex structures, and building reproducible quantitative scripts.

---

## 📂 Repository Structure

The active study files, interactive explanations, and quantitative models are organized by textbook:

* [Option_Future_James_Hull/Chapters/](file:///d:/projects/the_book_club/Option_Future_James_Hull/Chapters/)
  * `Chp15_Black_Scholes_Merton_Model.ipynb`: Stochastic modeling, pricing, and simulations.
  * `Chp7_Swaps.ipynb`: Comprehensive interest rate swap valuation and term structures.
  * `Chp9_XVAs.ipynb`: Advanced CVA, DVA, FVA, MVA, and KVA valuation frameworks.
  * `Chp10_Option_Mechanics.ipynb`: Exchange rules, CBOE margin accounts, and contract adjustments.
  * `Chp11_Stock_Option_Properties.ipynb`: Option properties, boundary inequalities, and Put-Call parity.

---

## 📈 Active Study: Options, Futures, and Other Derivatives
**Author**: John C. Hull  
**Status**: **[ACTIVE STUDY & IMPLEMENTATION]**

This is the current focus of the repository. I am actively translating Hull's definitive derivative pricing and risk management frameworks into highly visual, mathematically rigorous Python implementations.

### Replications & Implementations Completed:

#### 1. Stochastic Asset Price Modeling & The BSM Framework ([Chapter 15](file:///d:/projects/the_book_club/Option_Future_James_Hull/Chapters/Chp15_Black_Scholes_Merton_Model.ipynb))
* **Geometric Brownian Motion (GBM)**: Coded discrete-time path simulations ($dS_t = \mu S_t dt + \sigma S_t dW_t$) to visualize asset diffusion over time.
* **Volatility Drag**: Modeled how stochastic variance erodes geometric returns, numerically proving the drift adjustment of $\mu - \sigma^2/2$.
* **Risk-Neutral Valuation**: Programmed the Black-Scholes-Merton European option pricing formula.
* **American Option Dividends**: Implemented Black's Approximation to value early exercise boundaries on American dividend-paying contracts.

#### 2. Interest Rate Swap Valuation ([Chapter 7](file:///d:/projects/the_book_club/Option_Future_James_Hull/Chapters/Chp7_Swaps.ipynb))
* **Term Structure & Forwards**: Built zero-to-forward curve bootstrap calculations (under continuous compounding) for SOFR reference rate swap legs.
* **Discrete Rate Conversion**: Implemented continuous-to-discrete compounding frequency shifts ($R_c \to R_m$) to reflect realistic semiannual payments.
* **Portfolio of FRAs Valuation**: Valued an active swap (replicating Hull's Example 7.1) by isolating, netting, and discounting future cash flows.
* **Bond Replication Analogy**: Validated the cash-flow valuation against a replicated portfolio of long floating and short fixed bonds ($V_{\text{swap}} = B_{\text{fl}} - B_{\text{fix}}$).

#### 3. Advanced Valuation Adjustments - XVAs ([Chapter 9](file:///d:/projects/the_book_club/Option_Future_James_Hull/Chapters/Chp9_XVAs.ipynb))
* **Credit & Debt Valuation (CVA/DVA)**: Programmed counterparty default exposure adjustments, capturing the accounting "DVA paradox" during bank credit spread wiggles.
* **Funding & Margin Valuation (FVA/MVA)**: Explored the cost of funding variation margin (VM) and initial margin (IM) on bilateral vs. CCP cleared legs.
* **Fixed-for-Fixed Currency Swaps**: Valued cross-border currency legs (Examples 7.2 & 7.3) using both Forward Foreign Exchange contracts and dual-currency bond prices.
* **The Hurdle Debate**: Synthesized the core corporate finance debate surrounding average corporate funding hurdles vs. risk-adjusted marginal funding costs.

#### 4. Mechanics of Options Markets ([Chapter 10](file:///d:/projects/the_book_club/Option_Future_James_Hull/Chapters/Chp10_Option_Mechanics.ipynb))
* **CBOE Naked Margins**: Coded the exact CBOE margin rules (Calculation 1 & Calculation 2) for stock and broad-based index options.
* **Margin Profiles**: Plotted the CBOE Naked Put Margin requirement profile across different spot prices, showing the transition boundaries between Calc 1 and Calc 2.
* **Contract Adjustments**: Replicated Microsoft's 2004 special $\$3.00$ dividend option adjustments (scaling strike prices down and share counts up).
* **Payoff & Strangle Profiles**: Programmed interactive Python verifications for European option payouts, strangle profit profiles, and stock splits.

#### 5. Properties of Stock Options ([Chapter 11](file:///d:/projects/the_book_club/Option_Future_James_Hull/Chapters/Chp11_Stock_Option_Properties.ipynb))
* **Option Boundary Inequalities**: Coded mathematical call and put price bounds, demonstrating early exercise thresholds where the American put merges with its intrinsic value.
* **Put-Call Parity with Dividends**: Visualized no-arbitrage relationships for dividend-paying stocks and constructed synthetic option portfolios.
* **Butterfly Spread Payoffs**: Programmed option portfolio convexity proofs ($c_2 \le 0.5(c_1 + c_3)$) to visually demonstrate that the payoff of a butterfly spread is non-negative.
* **Arbitrage Exploitation**: Modeled complete, step-by-step risk-free cash flows for underpriced or overpriced calls and puts to exploit market inefficiencies.

---

## 🗺️ Upcoming Studies & Project Roadmap
Once the active study of John Hull's derivatives text is completed, the repository will transition to the following seminal works:

### Stage 2. Analysis of Financial Time Series **[PLANNED]**
**Author**: Ruey S. Tsay  
* **Volatility Forecasting**: Implementing GARCH, EGARCH, and CHARM models to capture conditional variance and asset clustering wiggles.
* **Linear Time Series**: Constructing ARMA/ARIMA forecasting models and analyzing multi-step forecast confidence limits.
* **Multivariate Econometrics**: Reviewing Vector Autoregressive (VAR) frameworks and co-integration for statistical arbitrage.

### Stage 3. Statistical Rethinking **[PLANNED]**
**Author**: Richard McElreath  
* **Bayesian Inference**: Coding Markov Chain Monte Carlo (MCMC) simulations using PyMC/Stan to compute posterior risk distributions.
* **Hierarchical Models**: Constructing multilevel models to pool information across sparse or highly diversified credit groups.
* **Causal Inference**: Mapping structural DAGs to isolate direct credit risk drivers and control for market confounders.

### Stage 4. Advances in Financial Machine Learning **[PLANNED]**
**Author**: Marcos López de Prado  
* **Alternative Data Labeling**: Coding the Triple-Barrier method and meta-labeling to capture clean trading signals.
* **Fractional Differentiation**: Implementing fractional calculus to make financial time series stationary while preserving maximum memory.
* **Financial Ensembles**: Customizing random forests and bagging algorithms to handle highly overlapping financial data.

---

## 🛠️ Stack & Environment
The code in this repository is built using clean, vanilla Python and standard scientific computing packages:
* **Core**: Python 3.10+, Jupyter Notebooks
* **Packages**: `numpy`, `pandas`, `scipy`, `matplotlib`
* **Environment**: Contained within local virtual environments (`.venv`) for maximum package reproducibility.