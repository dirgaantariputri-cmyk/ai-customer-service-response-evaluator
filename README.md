# AI Customer Service Response Evaluator

An AI-powered evaluation framework for analyzing the quality of customer service responses.

This project evaluates AI-generated customer service responses across six dimensions:

* Empathy
* Accuracy
* Professional Tone
* Helpfulness
* Clarity
* Made-up Information

The evaluator produces individual scores, an overall score out of 30, feedback, and an improved response.

---

## 🎯 Project Goal

Customer service AI should not only generate responses — its responses should also be evaluated for quality and reliability.

This project explores how an AI evaluator can identify:

* Poor customer service tone
* Lack of empathy
* Unsupported claims
* Made-up information
* Unhelpful responses
* Unclear communication

The project also experiments with improving the evaluation prompt itself.

---

## 🔄 Workflow

```text
Customer Complaint
        ↓
AI-Generated Response
        ↓
Evaluation Prompt
        ↓
Six Evaluation Criteria
        ↓
Individual Scores
        ↓
Overall Score / 30
        ↓
Feedback
        ↓
Improved Response
```

---

## 📊 Evaluation Criteria

Each response receives a score from **1 to 5** for each criterion.

| Criterion           | What it measures                                                |
| ------------------- | --------------------------------------------------------------- |
| Empathy             | Whether the response acknowledges the customer's feelings       |
| Accuracy            | Whether claims are supported by the available information       |
| Professional Tone   | Whether the response is respectful and appropriate              |
| Helpfulness         | Whether it provides useful assistance or a reasonable next step |
| Clarity             | Whether the response is easy to understand                      |
| Made-up Information | Whether the response invents unsupported information            |

### Scoring

| Score | Meaning    |
| ----- | ---------- |
| 1     | Very poor  |
| 2     | Poor       |
| 3     | Acceptable |
| 4     | Good       |
| 5     | Excellent  |

Maximum score:

**30 points**

---

## 🧪 Experiments

The project includes controlled experiments to test the evaluator.

### Experiment 01 — Strong Response

A strong late-order response received:

**30/30**

The evaluator identified appropriate empathy, accuracy, professionalism, helpfulness, clarity, and lack of fabricated information.

### Experiment 02 — Made-up Information

A poor late-order response containing unsupported warehouse, delivery, and contact claims received:

**13/30**

The evaluator correctly identified the fabricated information and lack of helpfulness.

### Experiment 03 — Professional Tone

A response containing dismissive language such as "You need to calm down" received:

**18/30**

The evaluator identified poor empathy and professional tone while recognizing that the response did not invent specific order details.

### Experiment 04 — Prompt V1 vs V2

Two versions of the evaluation prompt were tested against the same damaged-product response.

| Version | Score |
| ------- | ----: |
| V1      | 22/30 |
| V2      | 21/30 |

V2 gave a stricter score for made-up information after introducing more detailed scoring guidance.

This experiment demonstrates that **prompt design can influence evaluation results**.

---

## 📁 Project Structure

```text
ai-customer-service-response-evaluator/
│
├── examples/
│   ├── late-order.md
│   ├── refund-request.md
│   ├── damaged-product.md
│   └── angry-customer.md
│
├── experiments/
│   ├── experiment-01.md
│   ├── experiment-02.md
│   ├── experiment-03.md
│   └── experiment-04.md
│
├── prompts/
│   ├── evaluation-prompt.md
│   └── evaluation-prompt-v2.md
│
├── EVALUATION.md
└── README.md
```

---

## 🧠 Prompt Engineering Approach

The evaluation prompt was developed iteratively.

### Version 1

The initial prompt defined:

* Evaluation role
* Six criteria
* 1–5 scoring
* Output format
* Improvement feedback

### Version 2

The prompt was refined after testing to provide:

* Detailed scoring anchors
* Clearer accuracy definitions
* Stronger guidance around unsupported claims
* A distinction between accuracy and made-up information
* More consistent evaluation rules

This creates an iterative workflow:

```text
Prompt
  ↓
Test
  ↓
Observe Results
  ↓
Identify Weakness
  ↓
Refine Prompt
  ↓
Test Again
```

---

## 🔍 Key Findings

### 1. Professional does not always mean accurate

A response can sound polite and professional while making unsupported promises.

### 2. Clear does not always mean helpful

A response can be easy to understand while providing no meaningful solution.

### 3. Accuracy and fabricated information are related but different

Accuracy evaluates whether claims are supported and consistent.

Made-up Information specifically focuses on invented or unsupported facts, policies, actions, timelines, and outcomes.

### 4. Prompt design affects evaluation

The V1 vs V2 experiment showed that more detailed scoring guidance can change how an AI evaluator rates unsupported information.

### 5. Testing is necessary

A prompt should not be considered reliable simply because it looks well-written.

It should be tested against multiple response types.

---

## 🚀 Future Improvements

Potential next steps include:

* Add more customer service scenarios
* Test additional AI-generated responses
* Compare multiple evaluation prompt versions
* Introduce structured JSON output
* Automate evaluation using an API
* Calculate evaluation statistics across many responses
* Add a simple evaluation interface
* Compare AI evaluation scores with human ratings
* Measure evaluator consistency across repeated runs

---

## 💼 Portfolio Value

This project demonstrates practical experience with:

* Prompt engineering
* AI evaluation
* Customer service workflows
* Structured scoring systems
* Evaluation criteria design
* Prompt iteration
* Controlled experiments
* AI response quality analysis

The project progresses from **AI response generation** in Project 04 to **AI response evaluation and prompt optimization** in Project 05.
