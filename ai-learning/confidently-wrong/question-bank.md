# Question Bank

This document records the core MVP questions and how each maps an AI concept to a learning behaviour.

## Question 1 — How LLMs work

**AI topic:** LLM fundamentals  
**STOP skill:** Foundation  
**Difficulty:** Introductory

### Question
What is an LLM actually doing when it generates an answer?

### A
Searching its internal knowledge database for information that most closely matches your question.

### B
Predicting likely pieces of language based on patterns learned during training and the context you provide.

### C
Calculating which possible answer is most likely to be factually correct and then expressing it in natural language.

### Best answer
**B**

### Why
An LLM generates language by predicting likely tokens from learned patterns and available context. This can produce useful responses but is not equivalent to retrieving a verified fact or independently calculating truth.

### Takeaway
> **Fluent prediction is not the same as verified knowledge.**

---

## Question 2 — Fabricated citations

**AI topic:** Hallucinations / provenance  
**STOP skill:** SOURCE  
**Difficulty:** Introductory

### Question
An AI gives you a detailed answer, including the name of a research paper, the authors and the publication date. What should you assume?

### A
The citation is probably reliable because fabricating that much specific detail would be difficult.

### B
The information may be useful, but the citation should be independently verified before relying on it.

### C
Research citations are generally safer than ordinary AI answers because academic information is well represented in training data.

### Best answer
**B**

### STOP connection
**SOURCE — Where did this information come from?**

### Takeaway
> **A confident answer is not a source.**

---

## Question 3 — Current information

**AI topic:** Freshness / verification  
**STOP skill:** TRUTH  
**Difficulty:** Introductory–intermediate

### Question
You ask an AI assistant: "Who is the current CEO of Company X?" It gives an immediate answer. What's the best next question?

### A
How confident are you?

### B
Can you explain your reasoning?

### C
What current source are you using, and when was it published?

### Best answer
**C**

### Why
Current facts can change. Strong verification comes from current external evidence rather than the model's own assessment of confidence.

### STOP connection
**TRUTH — Can the important claim be independently verified?**

### Takeaway
> **For changing facts, freshness matters as much as confidence.**

---

## Question 4 — Causation and overconfidence

**AI topic:** Analysis / reasoning  
**STOP skill:** OVERCONFIDENCE  
**Difficulty:** Intermediate

### Question
You ask an AI to analyse why your company's sales dropped last month. It replies: "The decline was primarily caused by your recent price increase." The data shows sales fell after the price increase, but there is no evidence showing why customers bought less. What is the main problem?

### A
The AI has not calculated the size of the sales decline accurately enough.

### B
The AI has turned a possible relationship into a confident causal conclusion without enough evidence.

### C
The AI should avoid analysing business data unless it has access to the company's complete financial accounts.

### Best answer
**B**

### Why
Events occurring together or sequentially do not establish causation. The answer removes uncertainty from the language even though uncertainty remains in the evidence.

### STOP connection
**OVERCONFIDENCE — Is the AI more certain than the evidence allows?**

### Takeaway
> **Confidence is a writing style. It isn't evidence.**

---

## Question 5 — Confidential information

**AI topic:** Privacy / workplace AI  
**STOP skill:** PAUSE  
**Difficulty:** Intermediate

### Question
A colleague wants to paste a confidential client document into an AI assistant to summarise it. What's the best response?

### A
That's fine as long as they delete the conversation afterwards.

### B
First check whether the organisation has approved that AI tool and what its data-handling policy allows.

### C
Remove the client's name and the document will be safe to upload.

### Best answer
**B**

### Why
Data handling varies between products, plans and organisational deployments. The appropriate action is to follow approved tools and information-governance requirements.

### STOP connection
**PAUSE — What happens if this goes wrong?**

### Takeaway
> **The higher the consequence, the stronger the verification.**

---

# Final transfer challenge

**AI topic:** Evidence-based decision-making  
**STOP skill:** ALL  
**Difficulty:** Intermediate

### Scenario
You ask an AI:

"Our competitor says 73% of UK businesses will use AI agents by 2027. Should we accelerate our investment?"

The AI responds with a specific research citation, a precise statistic and a confident recommendation.

### Before acting, check:

**SOURCE** — Does the cited study exist and support the claim?  
**TRUTH** — Can the statistic be independently verified?  
**OVERCONFIDENCE** — Does one statistic justify a strong conclusion?  
**PAUSE** — What are the consequences of making an investment decision based on weak evidence?

### Best response
**Apply all four elements of STOP.**

### Final takeaway
> **You don't need to distrust AI. You need to know when to stop and check.**

## Future question-bank structure

Future questions can be tagged by AI topic and STOP behaviour, allowing later versions to identify **which type of AI judgement a learner finds difficult**.
