## README: Token Unlock Schedule with Dynamic Market Depth and Selling Pressure

### **Overview**
This Streamlit-based application provides an **interactive simulation and visualization tool** for projects involving **tokenomics**. It combines token unlock schedules, dynamic market depth, stochastic pricing models, and selling pressure triggers to help users analyze complex market scenarios and assess potential liquidity overflow risks.

---

### **Key Features**

1. **Configurable Tokenomics Parameters**  
   - Set **maximum token supply** and **initial token price**.  
   - Simulate price movements using:
     - **Constant Price Model**: Fixed token price for simplicity.
     - **Stochastic Price Model (Black-Scholes)**: Simulates token price volatility over time.

2. **Offset Simulation Start Month**  
   - Start unlock and price simulations at a specific month to align with real-world schedules.

3. **Customizable Vesting Schedules**  
   - Define and edit vesting schedules for multiple allocation categories (e.g., Pre-Seed, Team, Treasury).  
   - Add dynamic parameters such as:
     - **TGE (Token Generation Event)** percentage.
     - **Unlock rates**, lock-up periods, and start/end months.  
     - **Selling pressure triggers**: Adjust sell pressure when ROI (Return on Investment) surpasses defined thresholds.

4. **Bear Market Simulation**  
   - Specify **bear market periods** where token sell pressure increases due to adverse market conditions.  
   - Configure a **bear market coefficient** to simulate its impact.

5. **Dynamic Market Depth Simulation**  
   - Set initial **market depth thresholds** and simulate liquidity provisioning over time.  
   - Monitor how token unlock values interact with market depth.

6. **Overflow Detection and Analysis**  
   - Identify and visualize **overflow**: when token unlock values exceed available market depth.  
   - Analyze cumulative overflow values for specific month ranges.

7. **Rewards Allocation with Logistic Curve**  
   - Simulate rewards token distribution using a **logistic curve** to represent gradual unlock schedules.

8. **Interactive Visualizations**  
   - **Primary Chart**: Visualize token unlock schedules, overflow values, and market depth alongside stochastic price trends.  
   - **Secondary Chart**: Analyze ROI evolution, overflow, and bear market periods on a combined graph.  
   - Highlight key metrics with color-coded bars, shaded bear markets, and dynamic legends.

---

### **How to Use**

1. **Install Required Libraries**  
   Install Streamlit and dependencies:
   ```bash
   pip install streamlit matplotlib numpy pandas
   ```

2. **Run the Application**  
   Execute the script from your project directory:
   ```bash
   streamlit run app.py
   ```

3. **Configure Inputs via Sidebar**  
   - Set general tokenomics parameters (supply, prices, and start offsets).  
   - Configure vesting schedules, bear markets, liquidity provisioning, and rewards allocation interactively.  
   - Adjust simulation parameters like **volatility, return expectations**, and selling pressures.

4. **Interact with Visualizations**  
   - Monitor token unlock values, overflow risks, and price trends.  
   - Use sliders to focus on specific month ranges for cumulative overflow analysis.

---

### **Outputs and Visualizations**

1. **Token Unlock Schedule**  
   - Stacked bar charts display token unlock values for each allocation category.  
   - **Overflow areas** are highlighted when unlock values exceed market depth.  
   - A dynamic line chart overlays token price movements.

2. **ROI and Overflow Analysis**  
   - Visualize ROI evolution and overflow amounts over time.  
   - Bear market periods are highlighted with shaded regions.

3. **Cumulative Overflow Metrics**  
   - Use the slider to calculate and display cumulative overflow for specific month ranges.

---

### **Target Audience**
- Tokenomics strategists and financial analysts.  
- Crypto project teams managing token unlocks and liquidity.  
- Investors and stakeholders evaluating unlock schedules and overflow risks.

---

### **Technologies Used**
- **Streamlit**: For building the interactive user interface.  
- **Matplotlib**: For creating detailed and dynamic plots.  
- **NumPy**: For mathematical modeling, including stochastic simulations.  
- **Pandas**: For managing and editing vesting schedule data.

---

### **Disclaimer**
This tool is intended for simulation purposes and does not guarantee precise real-world outcomes. Users must validate inputs and results for their specific scenarios.

---

### **License**
MIT License.
