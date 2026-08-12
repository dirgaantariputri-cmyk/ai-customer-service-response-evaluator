# Experiment 04 — Evaluation Prompt V1 vs V2

## Objective

Compare two versions of the AI evaluation prompt using the same customer complaint and AI-generated response.

The purpose of the experiment is to determine whether the more detailed scoring guidance in V2 produces a meaningfully different evaluation.

## Test Input

### Customer Complaint

"My package arrived today, but the product is damaged. What can you do about this?"

### AI Response

"I'm sorry your product arrived damaged. We'll send you a replacement immediately, and you don't need to return the damaged item. Your new product should arrive within three days. Please send us a photo of the damage."

## V1 Result

| Criterion           |     Score |
| ------------------- | --------: |
| Empathy             |       5/5 |
| Accuracy            |       2/5 |
| Professional Tone   |       5/5 |
| Helpfulness         |       3/5 |
| Clarity             |       5/5 |
| Made-up Information |       2/5 |
| **Overall**         | **22/30** |

### V1 Findings

V1 correctly identified the unsupported replacement promise, no-return requirement, and delivery timeframe.

It considered the response strong in empathy, professionalism, and clarity.

## V2 Result

| Criterion           |     Score |
| ------------------- | --------: |
| Empathy             |       5/5 |
| Accuracy            |       2/5 |
| Professional Tone   |       5/5 |
| Helpfulness         |       3/5 |
| Clarity             |       5/5 |
| Made-up Information |       1/5 |
| **Overall**         | **21/30** |

### V2 Findings

V2 identified the same unsupported claims as V1 but scored the made-up-information criterion more severely.

The V2 scoring guidance specifically defines multiple concrete unsupported outcomes, policies, and timelines as serious fabricated information.

## Comparison

The two versions produced similar evaluations.

The main difference was:

**Made-up Information:**

* V1: 2/5
* V2: 1/5

**Overall:**

* V1: 22/30
* V2: 21/30

## Result

V2 produced a stricter evaluation of unsupported information while keeping the other criterion scores unchanged.

This suggests that the more detailed scoring guidance can improve calibration for responses containing multiple unsupported claims.

However, one experiment is not enough to establish that V2 is consistently better than V1. Additional test cases would be required.

## Conclusion

The experiment demonstrates that prompt design can influence AI evaluation results.

Adding explicit scoring anchors and clearer definitions can change how severely an evaluator rates unsupported information.

Future experiments should test V2 across additional response types to determine whether the improvement is consistent.
