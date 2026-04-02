**** Drying Process Analysis Under Data Constraints****
(Manufacturing Process Data Case Study)

**1. Problem**

- In a manufacturing drying process, production teams needed to better understand the conditions that lead to puffy drying outcome, while maintaining processing capacity and operational stability. However, the process did not have a direct sensor indicating drying outcomes in real time. Quality results were recorded separately by QC teams (batch & date level cause the machine dry continuously all day). It were not fully synchronized with process sensor data.
- The key business question became: How can we identify practical operating guidance for achieving puffy drying when the output condition is not directly measurable from process sensors?

**2. Challenges**

- No direct output indicator: There was no sensor directly indicating drying time, drying weight for puffy outcome, other outcome
- Data granularity mismatch: Process sensor data existed at high frequency (by minutes), while QC measurements were recorded at daily or batch levels.
- Imperfect time alignment: Exact drying windows could not always be mapped precisely due to operational recording limitations & estimate
- Incomplete process visibility: Some relevant contextual information (operational adjustments, calibration conditions, process disturbances) was not systematically recorded
- Real operational constraints: Production could not simply optimize one variable because of trade-offs between: Capacity, Energy consumption, Process stability, Product quality

This meant the goal was not theoretical optimization, but practical decision support under imperfect data conditions.

**3. Approach**

- Instead of attempting to build a strict predictive model, I focused on building a process understanding framework combining operational logic with available data signals.
- The approach consisted of 4 main steps:
  + Define drying episodes: Since no real-time drying classification existed, QC drying outcomes & machine operational logic were used to approximate drying periods.
  + Align process sensor data with production result: To deal with granularity mismatch, Process data was aggregated into representative operating ranges, sensor values were grouped into commonly used operating buckets, daily size measurements were used as a bridging variable --> Instead of exact matching, the analysis focused on identifying stable operational patterns.
- Identify operational patterns rather than correlations: Because of data limitations, statistical correlation analysis would have been misleading. Instead, the analysis focused on:
  + Observed operating patterns:
    - What ranges were commonly used during successful outcomes?
    - What trade-offs appeared between size and operating conditions?
    - Other conditions from upstream side
This reflects how real manufacturing decisions are often made: based on operational patterns rather than perfect statistical certainty.
- Frame results as decision trade-offs: Rather than searching for a single optimal setup, results were structured as trade-offs between: Input conditions (upstream), Material characteristics, Operating settings & Production capacity. The goal was to provide decision guidance, not absolute thresholds.

**4. Key Insights**
- Material size acts as a buffer for operational flexibility:
  + Larger material size provides more flexibility for maintaining higher operating speeds while supporting successful drying outcomes.
  + Smaller material size typically required: Lower feed rates, Lower material movement speeds, faster for fan, or compensating increases in energy consumption
--> This shows that upstream conditions strongly influence downstream operating freedom.
- Upstream decisions reduce downstream trade-offs: Analysis suggested that upstream input conditions affecting material size may be more effective leverage points than downstream process adjustments alone.
- In practice: Better upstream consistency → easier downstream operation
- Industrial data work is often about guidance, not certainty:
  + Due to real-world data limitations, the most valuable outcome was not a precise model but a structured understanding of:
    - What trade-offs exist
    - What options production has
    - What conditions reduce operational risk
--> This highlights an important reality of industrial analytics: Decision clarity often matters more than statistical perfection.

**5. Skills**

- Process understanding: Understanding how manufacturing behavior interacts with data signals.
- Data modeling, data anaylysis under imperfect conditions
- Operational thinking & Collaborate with related department
- Stakeholder-oriented analysis
- Problem solving under ambiguity

**6. Key Lessons Learned**

- Data rarely arrives in ideal form. Value often comes from structuring imperfect information.
- Process understanding is often more important than tooling.
- Good industrial analytics supports decisions, not just dashboards.

**7. Notes on Confidentiality**

To respect company confidentiality:
- Company identity is not disclosed
- Exact process parameters are omitted
- Internal dataset structures are not shown
- Numerical thresholds are generalized
--> This case focuses on methodology and thinking rather than proprietary information.
  
**8. Personal reflection**

This project strengthened my belief that strong data work is not about having perfect data, but about building enough understanding to support better decisions.
