# **Too Big to Terraflop: Minsky, Math, and the AI Bubble**

This document outlines the theoretical foundations of the simulation game "Too Big to Terraflop," explaining the economic theories of Hyman Minsky, the mathematical models used to gamify them, and the parallels to the 2025-2026 AI infrastructure boom.

## **A Note on the Title**

The title **"Too Big to Terraflop"** is a satirical play on the economic doctrine of **"Too Big to Fail."**

* **Original Concept:** "Too Big to Fail" refers to financial institutions (like massive banks) that are so deeply interconnected with the economy that their failure would trigger a systemic collapse. Consequently, governments and central banks are forced to bail them out, even if they are insolvent.  
* **The AI Twist:** In the context of 2025, the AI infrastructure build-out involves such astronomical sums of capital (trillions in data centers, chips, and energy) that it has become systemically critical.  
* **The Pun:** "Terraflop" serves a triple meaning:  
  1. **Compute Scale:** A reference to "Teraflops" (trillions of floating-point operations per second), the unit of measurement for the computing power driving the boom.  
  2. **The Crypto Echo:** A nod to the **Terra/Luna** collapse, a famous algorithmic "Ponzi" scheme that wiped out billions in days.  
  3. **The Terror:** Phonetically resembling "Terror-flop," capturing the panic phase of the Minsky cycle when the "invincible" investment thesis suddenly collapses.

## **1\. Hyman Minsky: Why Stability Breeds Instability**

**Hyman Minsky (1919–1996)** was an American economist who challenged the traditional idea that markets are naturally efficient and self-correcting. Instead, he argued that financial systems are inherently unstable and prone to crisis *because* of their periods of stability.

### **The Financial Instability Hypothesis**

Minsky’s core insight was that **"stability breeds instability."** During prosperous times, when cash flows are reliable, investors become complacent. They take on more risk and leverage, assuming the good times will continue forever. This transforms the market through three distinct stages of financing:

1. **Hedge Finance:** Borrowers can pay back both interest and principal from cash flows. (Safe).  
2. **Speculative Finance:** Borrowers can pay interest, but must roll over the principal. (Risky).  
3. **Ponzi Finance:** Borrowers cannot pay interest or principal from cash flows; they rely on rising asset prices to refinance or sell at a profit. (Dangerous).

### **The Minsky Cycle**

The game follows the classic five stages of a Minsky bubble:

1. **Displacement:** A new technology (AI) or innovation shocks the system, creating legitimate new profit opportunities.  
2. **Boom:** Smart money invests. Prices rise based on fundamentals.  
3. **Euphoria:** The general public and momentum traders enter. Prices decouple from reality. "Ponzi" financing becomes dominant.  
4. **Profit Taking / Distress:** Smart money sees the divergence and exits. The market stalls.  
5. **Panic:** A trigger (e.g., an earnings miss) causes a rush for the exits. Asset prices collapse below their true value.

## **2\. Game Design: Modeling the Madness**

To simulate this dynamic without needing thousands of individual agents, "Too Big to Terraflop" uses a **Representative Agent** model. We assume there are two massive pools of capital fighting for dominance, plus you (the player).

### **The Mathematical Framework**

#### **A. The Underlying Asset (Earnings)**

We model earnings ($E\_t$) not as a random walk, but as a convergence towards a hidden "Terminal Quality" ($Q$). However, we introduce a "Fraud" mechanic where bad actors mimic high-growth stocks before collapsing.

For a standard stock:

$$E\_t \= \\left( 20 \+ (Q \- 20\) \\times \\frac{t}{T} \\right) \\times \\text{Lognormal}(0, \\sigma)$$  
*Where* $t$ *is the current quarter,* $T$ *is total time, and* $\\sigma$ *represents market noise.*

For a "Fraud" stock:

$$E\_t^{fraud} \= \\begin{cases} 20 \+ 5t & \\text{if } t \< 5 \\text{ (Fake Growth)} \\\\ \\max(0, 45 \- 15(t-4)) & \\text{if } t \\ge 5 \\text{ (The Rug Pull)} \\end{cases}$$

#### **B. The Value Trader (The Anchor)**

Value traders represent the "Hedge Finance" mentality. They anchor to a fundamental truth: the Price-to-Earnings ($P/E$) ratio. We assume a "fair" P/E of 20\.

$$Demand\_{value} \= \\beta\_{val} \\times (20 \- \\frac{P\_t}{E\_t})$$

* If $P/E \< 20$, Demand is positive (Buy).  
* If $P/E \> 20$, Demand is negative (Sell).  
* $\\beta\_{val}$ is the sensitivity parameter.

#### **C. The Momentum Trader (The Bubble Maker)**

Momentum traders represent the "Speculative/Ponzi" mentality. They care only about the derivative of price—the trend.

$$Demand\_{mom} \= \\beta\_{mom} \\times \\left( \\frac{P\_t \- P\_{t-1}}{P\_{t-1}} \\right) \\times \\text{SentimentMultiplier}$$

* If price rose last quarter, they buy more.  
* **The Feedback Loop:** If they buy, price rises $\\to$ demand rises $\\to$ price rises further.  
* During the **Euphoria** phase (when market $P/E \> 40$), the SentimentMultiplier increases (e.g., 1.5x), simulating "Fear Of Missing Out" (FOMO).

#### **D. Price Dynamics (The Auctioneer)**

The price for the next quarter is determined by the net excess demand from all agents.

$$P\_{t+1} \= P\_t \\times (1 \+ \\alpha(D\_{value} \+ D\_{mom} \+ D\_{player})) \\times \\epsilon$$

* $\\alpha$: Price elasticity (how much price moves per unit of demand).  
* $\\epsilon$: A random log-normal shock representing exogenous market news.

## **3\. The 2025 AI Case Study: A Perfect Bubble?**

The game is set in the 2025-2026 AI boom because the current market exhibits textbook characteristics of a Minsky cycle.

### **The "Useful Technology" Paradox**

A common misconception is that bubbles only happen to useless things (like Tulips). In reality, **valid, transformative technologies create the biggest bubbles.**

* **Railways (1840s):** Revolutionized transport, but 90% of stock value was wiped out.  
* **Internet (2000):** Revolutionized information, but the NASDAQ fell 78%.  
* **AI (2025):** Will revolutionize intelligence, but valuations may still be detached from reality.

Because the technology is *real*, the "Displacement" phase is incredibly strong, convincing investors that "this time is different" and traditional valuation metrics (like P/E) no longer apply.

### **Evidence of the Bubble**

1. **Circular Revenue & The "Vendor Financing" Trap**  
   Much of the current revenue in the AI sector is circular.  
   * Big Tech Company A invests $10B in AI Startup B.  
   * AI Startup B uses that $10B to buy Cloud Services from Company A.  
   * Company A books this as "Revenue" and its stock soars.  
   * *Result:* Capital is moving in a circle, inflating valuations without generating external end-user profit.  
2. **Infrastructure Overbuild**  
   * Just as fiber-optic cables were overbuilt in the 1990s ("dark fiber"), we are seeing massive capital expenditure (CapEx) on GPUs and data centers. If consumer adoption of GenAI lags behind the pace of infrastructure build-out, these assets will depreciate rapidly, leading to the "Distress" phase.  
3. **"AI-Powered" Label Inflation**  
   * Similar to companies adding ".com" to their names in 1999, companies today slap "AI" on basic software to boost stock prices. This dilutes the quality of the market, making it harder to distinguish "Growth" stocks from "Mediocre" or "Fraud" stocks (a mechanic explicitly captured in the game).  
4. **Concentration & FOMO**  
   * The market is heavily concentrated in "Foundational Model" builders and hardware suppliers (e.g., Nvidia). The fear of missing out on the "next industrial revolution" forces funds to chase these stocks regardless of price, neutralizing the Value Traders until the inevitable earnings miss occurs.