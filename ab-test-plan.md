A/B Test Plan - The Landing Zone
Site: https://avmorris22.github.io/post-grad-move-guide/
Committed before any data was collected.

1. PAGE AND ELEMENT
Home page (index.html). I am changing only the main headline (H1).
Version A (current): "Your first big move, made manageable"
Version B (variant): "Just graduated and moving? Your first 30 days in a new city, planned."
Why: The headline is the first thing visitors read. My audience is recent graduates moving to a new city. A is warm but general. B names the visitor's situation and gives a specific time frame, so it should feel more relevant.

2. HYPOTHESIS
Version B will get a higher share of "yes, I would use this guide" answers than Version A, by at least 10 percentage points. This could be wrong if AI visitors respond to the page body and not the headline.

3. DESIGN
Visitors: an AI model, a fresh conversation for every trial, no memory between trials.
Model: Claude Sonnet 5.5, default settings, same for every trial.
Persona: a 22-year-old who just graduated and is about to move to a new city for a first job.
Exact prompt (same every trial except the page text): "You are a 22-year-old who just graduated college and is about to move to a new city for a first job. You found this page while searching for help with moving. Read the page below and decide whether you would use this guide to plan your move. Answer 'yes' or 'no' on the first line, then give one sentence of reasoning. [FULL PAGE TEXT]"
Assignment: before any trials, a random number generator makes the A/B order for all 120 trials and it is saved. Each trial uses its assigned version.
Protecting rankings: Version B is at index-b.html with a noindex tag and a canonical tag pointing to index.html, and it is not in sitemap.xml.

4. PRIMARY OUTCOME
Whether the visitor answers yes (1) or no (0) to: "Would you use this guide to plan your move?" Read from the first line of each response.

5. SAMPLE SIZE AND DATES
60 trials per version, 120 total, all collected before analysis. No stopping early.
Launch: November 10, 2026. Expected completion: November 14, 2026.
Any change after launch will be reported with the date and reason.

6. COMPARISON AND DECISION RULE
Two-proportion z-test (Fisher's exact if counts are small), two-sided, alpha 0.05. I will report both rates, the difference, and a 95% confidence interval.
Support for the hypothesis: B's yes rate is higher than A's and p < 0.05. Otherwise it is not supported, and I will report that honestly, including whether the test was too small.
