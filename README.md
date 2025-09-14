# Inventory Simulation and Policy Optimization

This project simulates a **non-terminating inventory system** governed by an **(s, S) ordering policy**.  
The objective is to identify the optimal inventory policy that minimizes the **long-run average total monthly cost**, considering ordering, holding, and shortage costs.

The work follows a **steady-state simulation approach**, since the system has no natural termination point. Statistical techniques such as **Welch’s method**, **replication/deletion approach**, and **confidence interval estimation** were applied to ensure valid steady-state performance evaluation.

---

## Methodology

This project applies a structured simulation approach to evaluate and optimize an **(s, S) inventory model** under uncertainty. The methodology integrates modeling, statistical analysis, and optimization as follows:

1. **Model Setup**  
   - Implement the (s, S) policy where orders are placed when inventory ≤ s, replenished up to S.  
   - Capture all relevant costs: **ordering**, **holding**, and **shortage costs**.  
   - Demand arrivals modeled as a **Poisson process** (Exponential inter-arrival times), while demand sizes follow an **empirical distribution**.

2. **Warm-Up Period**  
   - Identify and discard the initial transient phase using **Welch’s graphical method** to ensure unbiased steady-state estimates.  

3. **Replication-Based Statistical Analysis**  
   - Run multiple independent replications.  
   - Estimate mean monthly costs and construct **confidence intervals** for robust policy evaluation.  

4. **Optimization of Policies**  
   - Explore a **grid of feasible (s, S) policies**.  
   - Compare long-run costs across policies to identify the **cost-minimizing strategy**.  
 
---

## Results Highlights
- Optimal policies consistently found in the range **(s=50, S=90–100)**.  
- With longer runs and more replications, **(s=50, S=100)** emerged as the most cost-effective policy.  
- Confidence intervals narrowed significantly with increased replications and simulation length.  
- Ordering cost dominated (≈75% of total cost), followed by holding and shortage costs.  

---

##  Visualizations
1. **Determining the Warm-Up Period (Welch’s Method)**  
<p align="center">
  <img src="https://github.com/mandar-sk/Inventory_Model_with_Simpy/blob/main/images/Cumulative_Average_Inventory_Cost.png" width="700"/>
</p>

2. **Inventory Dynamics (s=50, S=100)**  
<p align="center">
  <img src="https://github.com/mandar-sk/Inventory_Model_with_Simpy/blob/main/images/Inventory_Level_Simulation.png" width="700"/>
</p>

3. **Contour Plot of Mean Monthly Cost**  
<p align="center">
  <img src="https://github.com/mandar-sk/Inventory_Model_with_Simpy/blob/main/images/Contour%20Plot%20of%20Mean%20Monthly%20Cost.png" width="700"/>
</p>

4. **3D Response Surface for Inventory Cost**  
<p align="center">
  <img src="https://github.com/mandar-sk/Inventory_Model_with_Simpy/blob/main/images/3D%20Response%20Surface%20for%20Inventory%20Cost.png" width="700"/>
</p>
