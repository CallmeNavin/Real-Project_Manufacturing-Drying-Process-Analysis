**What This Case Actually Felt Like**

**1. Problem**

- In a manufacturing drying process, production teams needed to better understand the conditions that lead to special drying outcome, while maintaining processing capacity and operational stability. However, the process did not have a direct sensor indicating drying outcomes in real time. Quality results were recorded separately by QC teams (batch & date level). So it cannot fully synchronized with process sensor data.
- The key business question became: How can we identify practical operating guidance for achieving special drying when the output condition is not directly measurable from process sensors?

**2. Challenges**

- No direct output indicator: There was no sensor directly indicating drying time, drying weight for special outcome
- Data granularity mismatch: Process sensor data existed at high frequency (by minutes), while QC measurements were recorded at daily or batch levels.
- Imperfect time alignment: Exact drying windows could not always be mapped precisely due to operational recording limitations & estimate
- Incomplete process visibility: Some relevant contextual information (operational adjustments, calibration conditions, process disturbances) was not systematically recorded
- Real operational constraints: Production could not simply optimize one variable because of trade-offs between: Capacity, Energy consumption, Process stability, Product quality

This meant the goal was not theoretical optimization, but practical decision support under imperfect data conditions.

**3. Approach**

- Instead of attempting to build a strict predictive model, I focused on building a process understanding framework combining operational logic with available data signals.
- The approach consisted of 4 main steps:
  + Define drying episodes: Since no real-time drying classification existed, QC drying outcomes & machine operational logic were used to approximate drying periods. Special drying time were used by QC sample collecting time
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
→ This shows that upstream conditions strongly influence downstream operating freedom.
- Upstream decisions reduce downstream trade-offs: Analysis suggested that upstream input conditions affecting material size may be more effective leverage points than downstream process adjustments alone.
- In practice: Better upstream consistency → easier downstream operation
- Industrial data work is often about guidance, not certainty:
  + Due to real-world data limitations, the most valuable outcome was not a precise model but a structured understanding of:
    - What trade-offs exist
    - What options production has
    - What conditions reduce operational risk
→ This highlights an important reality of industrial analytics: Decision clarity often matters more than statistical perfection.

**5. Engineer Diary**

- This project was not technically difficult because of algorithms. It was difficult because of data reality.
- At first, the expectation sounded simple: Understand what conditions lead to a successful special drying outcome.
- In reality, several structural limitations appeared immediately:
  + No direct sensor indicating drying outcome
  + QC data recorded manually and intermittently
  + No consistent mapping between QC timestamps and process sensor data
  + Batch information only available at coarse granularity
  + Machine calibration inconsistencies not always recorded
- This meant the problem was not: "How to analyze the data.". But the real problem was: "How to make a decision when the data structure itself is incomplete."

**5.1. First wrong assumption**

- Initially I assumed sensor mapping would be straightforward:
  + Match drying time → analyze sensors → derive conditions.
  + After merging datasets and checking distributions, inconsistencies appeared:
    - Some drying periods showed impossible sensor values.
    - Some mapped time windows did not align with actual process behavior.
    - This forced a shift in approach.
  + Instead of forcing correlations, I moved toward: Operational signal detection rather than statistical certainty.

**5.2. What changed the direction**

- The biggest realization was: this was not a modeling problem. This was a trade-off definition problem. Production was not asking: "What predicts special drying?". They were asking: 
"What must we trade if we want special drying without hurting capacity?". That reframed everything.

**5.3. What actually worked**

- Instead of trying to prove causation, I focused on:
  + Operating ranges actually used in production
  + Physical process logic
  + Small but consistent signals in noisy data
  + Constraints operators must respect
- From there the analysis became Not "What causes puffy drying?". But "Given how production really runs, what combinations are realistic?"

**5.4. The most important insight**

- In industrial data work:
  + Perfect data rarely exists.
  + What matters more is: Whether the analysis can still support decisions.
  + This case reinforced something important for me:
    - Data analysis in manufacturing is often not about finding the perfect answer.
    - It is about reducing uncertainty enough to allow action.

**6. Notes on Confidentiality**

To respect company confidentiality:
- Company identity is not disclosed
- Exact process parameters are omitted
- Internal dataset structures are not shown
- Numerical thresholds are generalized
→ This case focuses on methodology and thinking rather than proprietary information.
  
**7. Personal Takeaway**

- Technical skills help. But what mattered more here was:
  + Understanding process reality
  + Accepting data limitations
  + Framing decisions instead of forcing conclusions
  + Translating messy data into operational guidance
- The biggest learning was simple: Real data work is not about clean datasets. It is about staying useful when data is messy.
