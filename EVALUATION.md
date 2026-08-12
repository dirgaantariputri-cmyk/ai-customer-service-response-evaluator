# Evaluation Framework

## Purpose

This project evaluates AI-generated customer service responses against a consistent set of quality criteria.

The goal is to identify strengths, weaknesses, unsupported claims, and opportunities for improvement.

## Evaluation Criteria

Each response is evaluated using six criteria.

### 1. Empathy

Measures whether the response acknowledges the customer's feelings, frustration, or concern.

**High score:**

* Acknowledges the customer's situation.
* Shows understanding.
* Uses appropriate language for an upset customer.

**Low score:**

* Ignores the customer's frustration.
* Sounds dismissive or insensitive.
* Blames the customer.

### 2. Accuracy

Measures whether the response stays within the information provided.

**High score:**

* Uses only known information.
* Does not assume missing details.
* Does not make unsupported claims.

**Low score:**

* Claims to know information that was not provided.
* Makes unsupported promises.
* Assumes the cause or status of an issue.

### 3. Professional Tone

Measures whether the response is polite, respectful, and appropriate for customer service.

**High score:**

* Uses respectful language.
* Remains calm and professional.
* Avoids judgmental or dismissive wording.

**Low score:**

* Uses rude or dismissive language.
* Blames or insults the customer.
* Uses inappropriate expressions.

### 4. Helpfulness

Measures whether the response provides useful assistance or a reasonable next step.

**High score:**

* Offers a clear action.
* Requests information needed to investigate the issue.
* Gives the customer a useful next step.

**Low score:**

* Provides no meaningful assistance.
* Gives unsupported solutions.
* Leaves the customer unsure what to do next.

### 5. Clarity

Measures whether the response is easy to understand.

**High score:**

* Uses simple language.
* Is concise and direct.
* Clearly communicates the next step.

**Low score:**

* Is confusing or unnecessarily complicated.
* Contains irrelevant information.
* Makes the next step unclear.

### 6. Made-up Information

Measures whether the response invents information that was not provided.

For this criterion, a **higher score is better**.

**High score:**

* Does not invent facts.
* Does not create tracking details, delivery dates, explanations, or actions that were not provided.

**Low score:**

* Invents order information.
* Claims an action was taken without evidence.
* Gives unsupported delivery dates or explanations.

## Scoring System

Each criterion receives a score from **1 to 5**.

| Score | Meaning    |
| ----- | ---------- |
| 1     | Very poor  |
| 2     | Poor       |
| 3     | Acceptable |
| 4     | Good       |
| 5     | Excellent  |

The maximum score is:

**6 criteria × 5 points = 30 points**

## Score Interpretation

| Total Score | Interpretation                              |
| ----------- | ------------------------------------------- |
| 25–30       | Strong response                             |
| 19–24       | Good response with some improvements needed |
| 13–18       | Weak response with significant issues       |
| 6–12        | Very poor response                          |

## Important Evaluation Principle

A response should be evaluated based only on the information provided.

The evaluator should not assume facts that are not present in the customer complaint or AI response.

For example, if a customer only says that an order is late, the evaluator should not assume:

* Why the order is late
* Where the package is
* When it will arrive
* Whether the company contacted the delivery provider
* Whether a refund has been issued

This principle helps prevent the evaluator from rewarding or accepting unsupported claims.

## Evaluation Workflow

The project follows this workflow:

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
Overall Score
        ↓
Feedback
        ↓
Improved Response
```

## Current Experiments

The project currently contains three experiments:

* **Experiment 01:** Strong customer service response
* **Experiment 02:** Response containing made-up information
* **Experiment 03:** Response with poor professional tone

These experiments are used to test whether the evaluator can identify different types of response quality issues.
